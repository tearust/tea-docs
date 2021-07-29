# TEA Runs on Top of Blockchain
TEA itself is not a blockchain, but it is built on top of blockchain technologies. TEA uses blockchain as a layer-1 to provide

- Economical incentive and penalty that forms the basis of its token economy.
- Immutable trust information storage, such as credit history, key IDs and hashes.
- Block height as a universal clock between TEA nodes.

As explained in [TEA vs Blockchain](../What_is_TEA?/TEA_vs_blockchain.md)
> The TEA nodes runs above other blockchains. Any blockchain can send a computational oracle request in a blockchain event and receive the result along with PoT (proof of trust) in a tx at the later time.

In our milestone 1 demo, we use Substrate as our layer-1 blockchain provider. But this doesn’t mean TEA can only work with Substrate. In fact, any blockchain layer-1 with smart contract support will work with TEA, such as ETH etc. Of course, newer blockchain projects are prefered. That’s why we chose Substrate: it's written in Rust and WASM (the same tech that the TEA Project is built on), it's modern, fast and release-ready.

# TEA Works for Blockchain

TEA not only utilizes blockchain, but TEA also works as a layer-2 solution for layer-1. It can offload expensive and computationally complex tasks from layer-1, run the code in a trusted environment and send the result back to the blockchain together with verifiable Proof of Trust (PoT) data. In our milestone 1 demo, we run a Tensorflow image recognization algorithm offloaded from the blockchain. Have you ever dared run Tensorflow algorithm in a smart contract? Before the TEA Project, you'd have to have been crazy rich to try such a thing.

![lyaer1-and-layer2](https://github.com/tearust/tea-docs/blob/main/res/layer1-and-layer2.png?raw=true)

