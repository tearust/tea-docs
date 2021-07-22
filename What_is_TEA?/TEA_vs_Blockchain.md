# TEA Can Function as a Layer-2 Solution for Blockchains

The TEA project is built with Polkadot's substrate. Its essential consensus algorithm runs inside of our layer-1 blockchain component. TEA's layer-1 blockchain can function like a layer-2 oracle that runs on top of existing blockchains and act as a computation oracle for them. 

## TEA as a Computation Oracle For Other Blockchains
Smart contracts form the logical layer running inside of blockchains. You can use anything that happened previously in the block as input parameters for a smart contract function. But if some data happens outside of the blockchain, smart contracts need a way to trust this event. An [oracle](https://academy.binance.com/en/articles/blockchain-oracles-explained) is needed as the trusted input source. There are many kinds of oracles. TEA is a computation oracle that takes input from the blockchain, runs complex algorithms outside the chain, and then sends the computation result back to the chain. 

There are some good reasons why you don't do the computing inside blockchain:
- Complicated algorithms cannot run in smart contracts due to computational cost and time.
- Computational tasks often require additional hardware support such as a GPU or an AI TPU.
- Some functions need to run against big data which is not practical to run in blockchain nodes.
- Some functions need external data input from the real world. 

## Blockchain is the Client, and TEA is the Server
![relationship-between-layer1-and-2](https://github.com/tearust/tea-docs/blob/main/res/layer1-and-layer2.png?raw=true)

The diagram above shows how TEA nodes run on top of other blockchains. Any blockchain can send a computational oracle request in a blockchain event and receive the result along with PoT (Proof of Trust) data in a tx at a later time.

The request (we call it a task) is then submitted to the TEA network. One of the qualified executors will run the task under remote attestation by other qualified TEA nodes. The result is then returned back to the blockchain in the format of a transaction. Once the blockchain receives the answer, it can verify the PoT data returned and continue the smart contract logic.

The TEA Project has its own layer-1 blockchain (not shown in the diagram). This internal use layer-1 blockchain has the following purposes:
- Consensus on Proof of Trust.
- Token incentive logic.
- Key config and stats storage.

Based on this concept, we can consider blockchain as the client while the TEA Project is the server. 

## Verify PoT Between Chains
As a client, there are two concerns when using an external oracle.
- The result should be the exact computational result from the specific code and input data.
- There should be no data breach during the entire process.

TEA layer-1 is a blockchain running parallel with the client's blockchain. Inter-chain communication allows the client to send verification requests and get back confirmations. 

TEA's layer-1 is built using Polkadot's Substrate. Any blockchains compatible with Polkadot can easily integrate with the TEA Project in our early stages. Chains from all other platforms will be integrated at a future date.