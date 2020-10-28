TEA project design the T-rust platform based on existing technologies such as IPFS, Substrate blockchain, WebAssembly and Trusted computing. To summarise how we used them in a few bullets:
- Code and data all stored in IPFS
- Libp2p is the p2p network layer for both IPFS and T-rust
- The most important businese and consensus logic runs in the blockchain developed using Substrate.
- Most of T-rust system code and custom's code executes inside hardware protected trusted computing modules. TPM chips provide Proof-of-trust.
- 
# TEA vs IPFS
## TEA use IPFS as File System
Except for temporary memory cache, TEA modules do not allow to save anything on its local storage. Everything is required to store in the IPFS node which it connects to.
In this case, IPFS is the File System. Because IPFS is public accessable. Storing data on IPFS means everyone can access to it as long as the CID is known. In order to protect the data, everything stored to the IPFS need to be encrypted first. The encryption key will never store to IPFS or any persistent media. It stays in memory of the TEA modules. You may want to ask how others access to the data since it is encrypted and keys in the TEA module. Please read this link (TODO) to figure out.

## TEA extends IPFS by pluging-in trusted computing module so it can run code rather than store it.
Currently IPFS can only store data or code. Code is just a special format of data when it is not executing. If you dApp need to run the code stored in IPFS, you may have to either load into blockchain smart contract or a traditional cloud server (Lamda FaaS too) to execute. The former (smart contract) execution approach is limited by blockchain technology. The latter (traditional cloud computing) approach fall back to centralized world. For an example, if all the cloud service providers shut down all your servers, your dApp won't run although your code/code is still stay in IPFS undamaged. I personally consider those type of "dApps" just a hybrid dApps because it still rely on centralized servers to run, which we are trying to avoid.

TEA's solution is simple. Add a trusted computing module to existing IPFS node, turn it into a Function-as-a-service node. That's why we say
> Turn IPFS (File System) to new IPFS (Function-as-a-Service)

Rather than just ask IPFS to download a piece of code defined by CID, the clients can now ask IPFS (with TEA module) to *run* the piece of code (with or without input parameters) and return the result.

Immediately, you run into few questions:
- How do I verify if the result is correct?
- If the code is encrypted, how will the TEA module run the code? How about encrypted input data parameters?
- How do I know if the TEA module send the secrets thought some backdoor?

Let me explain in brief
### How do I verify if the result is correct?
IPFS client request a CID to the IPFS network, he doens't need to trust whoever response the content he requested for. Because he can easily verify the content by verifying the hash. If the hash match, this is the data that the request CID referred.

But the result of a code execution is unknown. You cannot verify the hash of the result to determine its correctness. In TEA, we do not verify the hash of result, but the hash of PoT (Proof of Trust). This is done in the blockchain layer-1. Only validated TEA nodes are allowed to host (we call pin) your code or data. Among those hosts, only [VRF](https://en.wikipedia.org/wiki/Verifiable_random_function) selected executor will actually run your code. The whole workflow is monitored by the blockchain smart contracts. The whole workflow is pretty complicated, read [this TODO]() to detail.    

### How can a TEA module runs code stored encrypted in IPFS?
TEA do not run [FHE](https://en.wikipedia.org/wiki/Homomorphic_encryption) algorithm against encrypted code. FHE is simple too expensive to be used practically. TEA modules' CPU run plain format of code because as long as the encrypted code enter the hardware protected TEA module, it will meet the encryption key there. So decrypt the data then run. Wait, wait, wait! How come the encryption key is here? The encryption key is supposed to be where the code was encrypted before post to IPFS? That's correct, but here is a missing piece: The [delegation chains consensus TODO]() distributes the key to other safe location during the "deployment workflow". In one sentence, qualified TEA modules can "pin" or "host" your code / data before it actually allow to run your code. The "qualification" process is called "Delegation" and it happens in the blockchain layer-1. Well, blockchain again. Did I say we are very close tie to blockchain although we claim we are not a blockchain.

### How do I know that the TEA module doesn't have a backdoor to steal my privacy?

[Trusted computing](https://en.wikipedia.org/wiki/Trusted_Computing) has been widely used for more than decades. You probably do not know that all computers and most cell phones produceds in recent 10 years have a small [TPM](https://en.wikipedia.org/wiki/Trusted_Platform_Module) chip on board. This tiny chip generate PoT (Proof of Trust) that get validated by other nodes through the consensus in the smart contracts on the blockchain. Using the combination of these technologies T-rust protects your privacy against breaching. 

## TEA uses LibP2P as network layer

LibP2P is part of IPFS project. TEA also use the LibP2P as the network layer of T-rust platform so that both IPFS and T-rust can share the network resources.

# Blockchain as layer1

Although T-rust builds on top of Substrate, and it does run a blockchain, we do not consider T-rust is a blockchain itself. It is more like a layer-2 oracle on top of existing blockchain. 
# Edge computing and 5G

# Use cases
## Defi

# Business models in decentralized era


