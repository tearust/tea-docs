# TEA is layer-2 solution for blockchain

TEA project ties to blockchain closely. A lot of essential consensus algorithm runs inside our layer-1 component - the blockchain we build using Polkadot's substrate. 

However, we do not consider T-rust is a blockchain itself. It is more like a layer-2 oracle on top of existing blockchain because the main purpose of T-rust is not to run a self blockchain, but to run a computation oracle for other blockchains. 

## T-rust as a computation oracle to blockchains
![oracle](https://m.media-amazon.com/images/I/41SRz47UbAL.jpg)
Smart contracts are the logic running in a blockchain. You can use anything happened previous in the block as input perameters for a smart contract function, but if some facts happened outside of the blockchina, smart contracts have no way to know or trust. Thus, an Oracle(https://academy.binance.com/en/articles/blockchain-oracles-explained) is needed as the trusted input source. This Oracle has nothing to do with the database or the company. There are many kinds of oracles. TEA is the computation oracle which takes input from the blockchain, run complex algorithm out of the chain, then send the computation result back to the chain. 

The reason why do not do the computing inside blockchain lays in the following facts
- Complicated algorithm cannot run in smart contract due to cost and time it may spend
- Some computational task required additional hardware's support. Such as GPU or AI TPU etc
- Some function needs to run against big data which not practical to run in blockchain nodes.
- Some function need external data input from the real world. 


## Blockchain is the client while T-rust is the server
![relationship-between-layer1-and-2](https://github.com/tearust/tea-docs/blob/main/res/layer1-and-layer2.png?raw=true)

See the diagram above. The TEA nodes runs above other blockchains. Any blockchain can send a computational oracle request in a blockchain event and receive the result along with PoT (proof of trust) in a tx at the later time.

The request (we call it a task) then submitted to the T-rust network. One of qualified executor will run the task under the remote attestation by other qualified TEA nodes. The result then return back to the blockchain in the format of transaction. Once the blockchain received the answer, it can verify the PoT (proof of Trust) then continue the smart contract logic.

T-rust has its own layer-1 blockchain (not shown in the diagram). It is for internal use. the main purposes of TEA layer-1 is for
- Consensus on Proof of Trust
- Token incentive logic
- Key config and stats storage

Based on this concept, we can consider blockchain is the client while T-rust is the server. 

## Verify PoT between chains
As a client, there are two conerns using an external oracle
- The result is exactly the computating result from the specific code and input data
- No data breaching during the whole process

TEA layer1 is a blockchain running parallel with the client blockchain. Inter-chain communication allow the client send verification request and get back the confirmation. 

TEA layer1 is build using Polkadot Substrate. Any blockchains compatible with Polkadot can easily integrate with T-rust at the first stage. Chains from all other platform will be integrated at a future time.

