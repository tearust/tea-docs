
![](../res/key-flows.png)
## Delegation Chain - Where the Data and Code Flow

The delegation chain is a network protocol. It guarantees that all the secrets are kept inside and are only transferred between verified trusted hardware modules. The protocol also maintains verifiable randomness when distributing the data to its hosts (we call it pin and repin). The entire data distribution flow can be traced by a series of signatures chained together, which is why it's called a delegation chain.

- A client sends secure data or code to a trusted TEA node as a delegator. If the client doesn't trust any other nodes, they would be best served owning a TEA node so that they will act as a delegator for their own data or code.
- A delegator will be looking for qualified executors among all the TEA nodes in the IPFS p2p network. Remote attestation is done between each node before exchanging any sensitive information
- Data or code will be transferred via a **repin** to a new delegator (called a **pinner**) to host, or to an executor to run.
- No matter where the data or code goes, the proof of delegation (PoD) will be attached at each step. It therefore becomes a delegation chain.
- Anyone can verify the delegation chain from the latest step all the way up to the first delegator or the client to make sure the chain is valid. Any hacks in the middle would be easily discovered via the blockchain.
- TEA's layer-1 blockchain will be used to do the verification. Any incentives or punishments is then applied to the participating nodes.