# TEA runs on top of blockchain
As I mentioned above, TEA itself is not a blockchain, but it is built on top of blockchain technologies. TEA uses blockchain as layer1 to provide

- Economical incentive and penalty, token economy.
- Immutable trust information storage, such as credit history, key IDs and Hashes
- Block height as a universal clock between TEA nodes

In our milestone 1 demo, we use Substrate as our layer 1 blockchain provider. But this doesn’t mean TEA can only work with Substrate. In fact, any blockchain layer1 with smart contract support will work with TEA, such as ETH etc. Of course, newer blockchain project is prefered, that’s why we choose Substrate first because it is written in Rust and Wasm (We are too), it is modern, fast and release-ready (at the time we start coding).

# TEA works for blockchain

TEA is not only to utilize blockchain, but TEA also works as a Layer 2 solution for layer1. It can offload expensive and complex computation from layer1, run the code in a trusted environment and send the result back to the blockchain together with verifiable Proof of Trust (PoT as we called). In our milestone 1 demo, we run a Tensorflow image recognization algorithm offload from the blockchain. Have you ever dare to run Tensorflow algorithm in a smart contract? You must be crazy rich!

![lyaer1-and-layer2](https://github.com/tearust/tea-docs/blob/main/res/layer1-and-layer2.png?raw=true)

As explained in [TEA vs Blockchain](../What_is_TEA?/TEA_vs_blockchain.md)
> The TEA nodes runs above other blockchains. Any blockchain can send a computational oracle request in a blockchain event and receive the result along with PoT (proof of trust) in a tx at the later time.


![](/img/Under_Construction_Tape.png)