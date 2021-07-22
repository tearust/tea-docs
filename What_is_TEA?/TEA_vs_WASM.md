# TEA and WebAssembly

WebAssembly (WASM) is a newly designed portable and virtual ISA. There are many features worth a separate lengthy post, but let's focus on some of its security features.

## WASM Security Features

- Isolation.
- Linear memory.
- Table of functions.
- Interface (WASI).
- Type.

Let's look at a small example to see how these security features come together. A typical application has access to some system resources such as read/write folder privileges and socket connections. If the executable has access to these system services, then its entire process has access. Developers usually use 3rd party open source libraries in their projects. If any of those libraries have vulnerabilities, the hacker can control the process to read/write some security information and send it back through the network. Do developers check every line of open source library they import to their project? That's probably not possible for most projects of any size. If the code is running inside a TEE (Trusted Execution Environment), and the code itself is malicious, then the TEE can't help. But this is a scenario where WASM can provide some protection.

## Putting the WASM Runtime Inside TEE Sounds Like a Good Idea

We already have TPM, TEE, and WASM; how about putting them all together?
If the WASM runtime executes inside TEE, outsiders (even the OS) cannot access any secrets inside. For the TPM/HSM solution, the computing machine is protected by the TPM, so we know it's what it's claiming to be. For the TEE solution, the CPU chips provide protection via manufacturer validation. The node itself is the client or a CDN node or IPFS node that stores the data.

Developers no longer need to deploy the server function code to cloud computing service providers. They upload their static resources (app binary or HTML/CSS/JS/WASM) to IPFS or a CDN. Client apps do not need to upload their user data to the cloud server. They just send request data to nearby computing nodes that cache code. The node makes the computing inside its TEE and returns the result with proof of trust (PoT) data. The client machine can also become a compute node if equipped with TEE. Because there is PoT data, everyone can verify this compute result, and the process can be trusted by remote attestation.

## Since WASM is Portable, Can We Leave Data Where It is and Send Bytecode Over?

WASM is designed to be portable and secure. It could (very likely) be used as a general-purpose edge computing compile target. When we typically deploy server code to cloud computing data centers, clients upload their data to the same server. When code and data meet up, the CPU does the computing, and the result is sent back to the client. That setup is acceptable for small amounts of data. What if the data to be computed is large enough to be sent over the backbone network? When 5G becomes popular, the last-mile bandwidth becomes much more considerable. Given that AI needs lots of data to parse, will our backbone or data center be able to handle that much traffic? Probably not. Instead, we can leave the data where it is but send the code (algorithm or function) to the data. The data and code meet together and are computed not at the data center but where data is stored. The code usually is much smaller than the data in this scenario. We not only save the backbone bandwidth but also reduce latency from the client's experience.

This is all wonderful, but none of it will be useful until we're able to solve our trust issue. What is the trust issue? Well, we can trust Amazon, so we can trust the result from the AWS server. But we cannot simply trust any random client or edge computing node. If there is no way to protect the security of data or code, the chances are that **a)** the result may be incorrect or **(b)** the sensitive data could leak.

## All-in-one Solution: A HSM to Put Everything Inside, Plug & Play

Not all CDNs or IPFS miners' boxes are equipped with all the hardware they need to join the TEA network. A good business idea would involve making a small plug-and-play HSM (Hardware Secure Module) that contains everything a miner would need. Miners plug it into their IPFS box, and voila! The storage node becomes an edge computing node! Besides mining Filecoin, this machine can mine [//TEA] as well.

More information on the relevant hardware-related topics ( HSM, TEE, and TPM) is explained in [TEA vs Trusted Computing](TEA_vs_Trusted_Computing.md).

# TEA is Based on waSCC, an Awesome WASM Runtime on the Server

WaSCC, [wascc.dev](https://wascc.dev), is a dynamic, elastically scalable WebAssembly host runtime for securely connecting actors and capability providers. TEA uses waSCC (with small modifications) as the
WASM runtime inside TEA modules. You can check the TEA node internal diagram to see where the runtime is positioned.

![tea-node-internet-arch](https://github.com/tearust/tea-docs/blob/main/res/tea-node-arch.png)

## Security

WaSCC is well structure and designed. If you read the wsSCC documents, you should get an idea of why wsSCC is very secure. Beyond that, the TEA Project adds some additional security features.

When a TEA node boots, hardware TPM chips verify everything, including the hash of the runtime binary. It will report the hash of the current running runtime executable. Suppose some TEA node is running a different runtime that's not recognized by the consensus of the blockchain. It will be marked "suspicious" and later removed from the TEA network. "Remove" in this sense means that the code becomes "isolated" or "quarantined." This prevents bad TEA nodes from causing damage.

Most of TEA consensus logic runs either in the layer-1 blockchain as smart contacts or as WASM actors in the TEA runtime. The runtime will verify every actor and provider before loading. This verification is not waSCC's built-in signature verification but a hash stored in TPM chips and on the blockchain. This node may be quarantined if any actor or provider's hash doesn't match its claim on blockchain or TPM records.

Once the boot and init have completed, other TEA nodes can verify by running a remote attestation process. The truth comes from the TPM and the blockchain. Any component that doesn't match what's claimed will be detected.

If the TEA node chooses to use CPU's TEE instead of the TPM, the validation is done by the CPU manufacturer. We can still use TPM to ensure the correct code is loaded, but the sensitive data will be processed inside the CPU's enclave. More about trusted computing is available [here](TEA_vs_Trusted_Computing.md).

## Provisioning
The drawback of WASM's stability is that there are limited opportunities to update the runtime. The runtime binary can even be "hardened" to the hardware, as is the case with SoC (Software on Chip). When the TEA node starts, it read the records from the blockchain, gets the CID of each actor and provider, and downloads these actors and providers from a connected IPFS server. This sign makes to pre-install runtime without any "moving parts." All moving parts can be obtained from IPFS by CIDs from the blockchain. Always the latest version and secure.

## TEA Upgrades
A TEA module exists as physical hardware owned by its owner, but what runs inside of it is not controlled by the owner. Any individual or company can't control it. It is instead run the blockchain governance, specifically a [DAO](https://en.wikipedia.org/wiki/Decentralized_autonomous_organization). A committee is elected to make decisions that are enforced by smart contracts. 

Once a new version of an actor passes the smart contract validation, the CID of this actor will be announced on the blockchain. Based on the grayscale algorithm, TEA nodes will be required to upgrade tier by tier. The upgrading TEA node gets the CID from the blockchain, downloads the actor's binary from IPFS, refreshes and reloads it into memory. Once the new upgraded configuration passes the other TEA nodes' remote attestation, this TEA node will then be activated to serve on the network again.

## Platform Independent

Platform independence is an original feature of WASM. TEA integrates the WASM runtime on our platform because we want the TEA platform to run on almost any kind of CPU architecture. A commonly asked question is why doesn't the TEA Project use Intel SGX technology as its TEE. A simple answer is that we believe that trusted computing needs to run on different kinds of architecture, not just on a specific brand. Edge computing, IoT, and AI all require different kinds of technologies compared to those used in PCs, Macs, and servers. The future of CPU architectures could be very fragmented, not to mention the new kid in the block: RISC-V. TEA's use of WASM gives it platform independence and flexibility to run on the CPU architectures of the future.

## WASM Resources

WASM is also known as WebAssembly, but don't be fooled by its name. Some good WASM resources include [Webassembly, Neither Web, Nor Assembly, but Revolutionery](https://www.javascriptjanuary.com/blog/webassembly-neither-web-nor-assembly-but-revolutionary) is a good read or the following introductory [video on YouTube](https://www.youtube.com/watch?v=UtjoaTfbdcA) for those new to WASM. 