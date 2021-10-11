      

The TEA Project’s goal is to provide a platform where rich, decentralized applications can run at native speeds across a decentralized network of computing nodes. It solves the Blockchain Trilemma by offering a scalable, decentralized, and secure blockchain without compromising any one aspect.

![](_1-trilemna.png)

The TEA Project builds on many emerging projects and paradigms which in and of themselves are not sufficient to solve the Blockchain Trilemma.

The concept of trusted computing has been stuck in the limiting paradigm of one-computer = one-metal-box that limits its expansion and possible uses cases in a distributed world. It needs the help of blockchain and other emerging technologies to expand beyond its current barriers.

In the TEA Project, computing nodes become trusted through a Remote Attestation process. This elevated node is now trustable to store and transmit sensitive information and securely run WebAssembly code.

  

-   Blockchains like Ethereum provide a world computer where smart contracts can run in a decentralized manner. They are further augmented by Web3 innovations like IPFS, a peer-2-peer file system that stores files in a decentralized manner.

[Link to IPFS for more info](./IPFS.md)


But smart contracts by themselves cannot currently run complex algorithms. Attempts to do so have shown smart contracts to be too slow or too expensive as they lack the processing power compared to modern cloud computers. A layer-2 solution would be needed to offload the computation tasks as long as it could provide a similar trust level as the layer-1 blockchain.

**Byzantine-fault tolerance leads to slow processing** 

No matter how many nodes are running in a typical blockchain system, the one-by-one ordered transaction queue of existing Byzantine fault tolerant (BFT) consensus algorithms leads to slow data processing times. Smart contracts currently cannot run complex algorithms. Attempts to do so have shown smart contracts to be too slow or too expensive as they lack the processing power of modern cloud computers. 

Existing blockchains are slow because they need BFT to reach consensus. They could host dApps that reach the speed of cloud computers if only they had trust. Trust is exactly what the TEA Project is able

 We don't yet have rich dApps running at cloud-speed on blockchains since these systems need consensus to guard against a trust-less environment. Cloud computing gives you rich and fast apps, but it's not decentralized and you must assume their ecosystem is trustable.

But what if trust is already taken care of? Then our blockchain could implicitly trust its nodes and use (Raft consensus). Our blockchain would run fast like cloud computers who are able to take trustable nodes for granted.

## The TEA Project Solves the Blockchain Trilemma to Deliver Decentralized, Secure, and Scalable Apps

## Decentralization

The TEA Project’s decentralized TApps run on decentralized miners that connect to each other through a peer-to-peer network. Every TEA node is protected and monitored by hardware TPM chips or the CPU's TEE (Trusted Execution Environment) which provides PoT (Proof of Trust) data. 

Every TEA node can reference this PoT data for every node participant to verify any individual TEA node's integrity through a Remote Attestation process completed through smart contracts. Nodes in the TEA network are incentivized by the token economy to perform Remote Attestation verification.

## Security

The hardware security modules allow the compute nodes to offer a hardware-protected enclave where code and data can securely run. Due to limited resources inside the protected enclave, developers must decide which functions need to run inside the enclave for security and which functions should run outside the enclave to gain performance.

[Link to more info on TEA hardware mining modules](./Miners.md)

Anyone outside the TEA module's hardware has ZK (Zero-Knowledge) about what happens inside the module. Neither the TEA node's owner nor the server connected to the module will know, nor can anyone predict which node is running any particular task. Because these are all zero-knowledge algorithms, no information can be breached during this secure workflow.

The TEA Project's goal is to build a platform that allows code and data to run inside trusted TEA modules without needing to trust anything else. The technologies built into the TEA platform protects the data and the integrity of the result.

The computation is based on the expected code and expected data. No one can alter the input code, the input data, or the output result.

The result of the computation is correct given the computing environment is verified through Proof of Trust data that is shared in the network and verified via Remote Attestation.

There's no chance of data breaches during the entire process.

## Scalability

In the TEA Project, trust solves the scalability issue by opening up a second blockchain where every node is trusted.

Typically only centralized cloud computing can use (Raft consensus) as a single company is able to oversee all of the computing nodes. That allows cloud computing companies to be scalable and secure (as long as you trust the company). But we can’t totally trust our data with these companies as they are centralized and are typically not transparent with their data safeguards.

The TEA Project solves scalability by using non-BFT consensus (Raft) to run TApps on a fast layer-2 blockchain.

- The TEA Project uses layer-1 to run BFT to filter out all non-trustable nodes.  
- The layer-2 blockchain can check the trust status of any of its nodes by querying the layer-1 blockchain.  
- The TEA Project's layer-2 can now use the much faster (Raft consensus) because it can assume all its nodes are trustable as reported by the layer-1 blockchain. 

## Developers and Code

In the current cloud computing model, trust is needed between developers, cloud service providers and the end client.

Let's assume that a consumer has valuable and sensitive data such as health data output from wearable tech. It needs an algorithm to make sense of the data, and computing power to run the cod. There are algorithms (code) created by developers that can do this job very well. The consumer wants to run the code with their data as input. Additionally, you don’t trust the developers or service providers who host the code due to a concern about possible data breaches.


(Graphic of TEA Project use case)

  
## Developers Funding

Developers can use TEA Project’s built-in bonding curve to generate investment in their TApp. This funding mechanism allows TApps to leverage expected future revenue into early development funding. The TAppStore is where the entire TEA ecosystem meets: developers to publish their TApps, miners can find the next TApp to invest their harvested TEA tokens, curators to publicize and invest in new trending TApps, and consumers to spend their TEA tokens on useful TApps they want to use. 

Developers can use their favorite programming languages and compile their code into WebAssembly, the native languge of TApps.