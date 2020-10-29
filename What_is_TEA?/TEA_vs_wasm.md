# Tea vs WebAssembly

WebAssembly (WASM). Do not get fooled by its name, [Webassembly, Neither Web, Nor Assembly, but Revolutionery](https://www.javascriptjanuary.com/blog/webassembly-neither-web-nor-assembly-but-revolutionary) is a good read or [watch](https://www.youtube.com/watch?v=UtjoaTfbdcA) in case it is new to you. 

It is a newly designed, portable virtual ISA. There are so many features we can talk about but let's just list a few features related to security:

- Isolation
- Linear memory
- Table of functions
- Interface (WASI)
- Type


There are more features worth a separate long blog to talk about. I will just give you one small example for now.

If an application has access to some system resources (such read/write a folder, socket connection, etc.), the whole process has access. Developers usually use 3rd party open source library in the project. If any of those libraries have vulnerable, the hacker can control the process to read/write some security information then send it back through the network. Do developers check every line of open source library they import to his project? Probably not, or cannot. Then even the code is running inside TEE, the code itself is an evil, TEE cannot help. But Wasm can help with this. Thanks, awesome WASI team! For detail, please wait for my future blog on this.

## Since Wasm is portable, can we leave data where it was, we send bytecode over?
Wasm is designed to be portable and secure. It could (very likely) to be used as a general-purpose edge computing compile target.

Nowadays, when we typically deploy server code to cloud computing datacenter, then client upload their data to the same server. When code and data meet together, the CPU does the computing, then the result is sent back to the client. Nothing wrong for today's small data size. What if in the future, the data to be computed is huge enough to be sent over the backbone network? When 5G becomes popular, the last-mile bandwidth become much bigger, and AI need tons of data, will our backbone or datacenter handle the traffic? Probably not. Why do not we leave the data where it was, but send the code (algorithm or function) to the data. The data and code met together and computed not at the datacenter, but where data was stored. The code usually is much smaller than the data in this scenario. We not only save the backbond bandwidth but also reduce latency from the client's experience.

Wait for a minute, it won't be useful until we can solve the trust issue. What is the trust issue? Well, we can trust AWS, so the result from the AWS server can be trusted. But we cannot simply trust any random client or edge computing node. If there is no way to protect the security of data or code, chances are (a)the result may not be correct, or (b)the sensitive data leaking or both.

## Put wasm runtime inside TEE sounds a good idea

We already have TPM, TEE, Wasm, how about we put them together?
Wasm runtime executes inside TEE so that we know outsiders (even the OS) cannot access the secret inside. The computing machine is protected by the TPM so that we know it is what it claimed to be. The node itself is the client or a CDN node or IPFS node, which stored the data.

Developers no longer need to deploy the server function code to cloud computing service providers. They upload their static resources (app binary or HTML/CSS/js/wasm) to IPFS or CDN. Client apps do not need to upload their user data to the cloud server, it just sends requests to nearby computing node which caches code. The node makes the computing inside its TEE and returns the result with proof of trust (PoT). The client machine also can also become a compute node if equipped with TEE. Because there is a PoT, everyone can verify this compute result and process can be trusted by remote attestation.

## All-in-one solution: A HSM to put everything inside, plug and play
Not all CDN or IPFS miners' boxes are equipped with what we need. A valid business idea probably would be to make a small plug-and-play HSM (Hardware Secure Module) which contains everything we need. Miners just plug it in the IPFS box; the storage node soon becomes an edge computing node! Besides mining Filecoin, it can mine "ComputeCoin" as well.

The hardware related topic, such as HSM or TPM, is explained in [TEA vs Trusted Computing](TEA_vs_trusted_computing.md).

# TEA is based on waSCC, an awesome WASM runtime on the server

WaSCC, [wascc.dev](https://wascc.dev), is a dynamic, elastically scalable WebAssembly host runtime for securely connecting actors and capability providers. TEA use wsSCC (with small modifications) as wasm runtime inside TEA modules. You can see the TEA node internal diagram to see where the runtime is positioned.

![tea-node-internet-arch](https://github.com/tearust/tea-docs/blob/main/res/tea-node-arch.png)

## Security

WaSCC is well structure and design. If you read the wsSCC documents, you should get the idea why wsSCC is very secure. Beyond that, we add some additional security features.

When TEA node boots, hardware TPM chips verify everything including the hash of runtime binary. It will report what the hash of the current running runtime executable. Suppose some TEA node is running a different runtime that not recognized by the consensus of blockchain. It will be marked "suspicious" and later removed from the TEA network. "Remove" not physical remove. It just means "isolated" or "quarantine". No damage a bad TEA node can make in such case.

Most of TEA consensus logic runs either in the layer-1 blockchain as smart contacts or the wasm actors in the tea-runtime. Every actors and provider will be verified by runtime before loading. This verification is not waSCC built-in signature verification, but a hash stored in TPM chips and blockchain. Again if any actor or provider hash doesn't match its claim on blockchain or TPM records, this node may be quarantined.

Once the boot and init completed. Other TEA nodes can verify by running a remote attestation process. The truth comes from the TPM and blockchain. Any component doesn't match claim will be detected.

## Provisioning

Since the runtime itself is stable so that in the future we may have a scarce chance to update runtime. The runtime binary can even be "hardened" to the hardware as SoC (Software on Chip) in the future. When the TEA node starts, it read the records from the blockchain, then get the CID of each actor and providers. Download these actors and providers from connected IPFS server. This sign makes to pre-install runtime without any "moving parts". All moving parts can be obtained from IPFS by CIDs from the blockchain. Always the latest version and secure.

## Upgrade

Although TEA modules is physically owned by its owner, What is supposed to run inside are not controlled by the owner. Any individual or company can not control it. It is by the blockchain governance. The concept is called [DAO](https://en.wikipedia.org/wiki/Decentralized_autonomous_organization). A committee is elected to make such decision and enforced by smart contracts. Once a new version of an actor passes the smart contract validation. The Cid of this actor will be announced on the blockchain. Based on the grayscale algorithm, TEA nodes will be required to upgrade tier by tier. The upgrading TEA node gets the Cid from blockchain, download the actor binary from IPFS, refresh and reload into memory. Once the upgrade new configuration passes other TEA nodes' remote attestation, this TEA node is active to serve again.

## Platform independent

This is original the feature of WASM. We reclaim here because we want the T-rust platform can run in most kinds of CPU architecture. A commonly asked question is why we do not use Intel SGX technology as our TEE. A simple answer is we believe the trusted computing needs to run on different kinds of architecture, not only a specific brand. Especially edge computing, IoT, AI all requires different kinds of technologies that those used in PC/Mac/Servers. The future of CPU architecture could be very fragment, not to mention the new kid in the block: RISC-V. We design for tomorrow, not today.






