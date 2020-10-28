TEA project design the T-rust platform based on existing technologies such as IPFS, Substrate blockchain, WebAssembly and Trusted computing. To summarise how we used them in a few bullets:
- Code and data all stored in IPFS
- Libp2p is the p2p network layer for both IPFS and T-rust
- The most important businese and consensus logic runs in the blockchain developed using Substrate.
- Most of T-rust system code and custom's code executes inside hardware protected trusted computing modules. TPM chips provide Proof-of-trust.
- 

## TEA extends IPFS by pluging-in trusted computing module so it can run code rather than store it.
Currently IPFS can only store data or code. Code is just a special format of data when it is not executing. If you dApp need to run the code stored in IPFS, you may have to either load into blockchain smart contract or a traditional cloud server (Lamda FaaS too) to execute. The former (smart contract) execution approach is limited by blockchain technology. The latter (traditional cloud computing) approach fall back to centralized world. For an example, if all the cloud service providers shut down all your servers, your dApp won't run although your code/code is still stay in IPFS undamaged. I personally consider those type of "dApps" just a hybrid dApps because it still rely on centralized servers to run, which we are trying to avoid.

TEA's solution is simple. Give every IPFS node who is willing to join T-rust network
# Blockchain as layer1

Although T-rust builds on top of Substrate, and it does run a blockchain, we do not consider T-rust is a blockchain itself. It is more like a layer-2 oracle on top of existing blockchain. 
# Edge computing and 5G

# Use cases
## Defi

# Business models in decentralized era


