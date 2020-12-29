# Where does the trust of T-rust come from?

If you have not read my previous blogs about the Tea Project and the T-rust framework, let me briefly introduce the relationship between those concepts.

The TEA Project is a team of developers building a decentralized framework and applications based on trusted computing and blockchain. 

T-rust is the name of the framework that other applications can run on top. Because T-rust is so far (and likely continue to be) the only framework in the TEA project, sometimes we use TEA refers to T-rust. So all of the following statements are valid:

- I am a TEA project developer.
- Gluon and T-rust are two TEA projects.
- Gluon is a TEA application.
- My application is running on TEA. 
- My application is running on T-rust.

Gluon is the first application we build on top of T-rust except for the previous first demo app, which runs Tensorflow AI on the blockchain. We are confident that there will be more applications running on top of T-rust in the future. But why do applications run on top of TEA rather than run directly on top of the blockchain or a cloud-computing server?

## Why do they not run on the blockchain or cloud?

If your application is not intended to be a decentralized app, it should be running in the cloud. It is cheap and fast. The only caveat is that all 3 parties (developers, service providers, and clients) have to either have some trust or just blind trust. There are many ways to get some trust from outside, such as the developers hired by the company who use their code, or the service providers are big names that you can easily trust by nature; Blind trust is also a kind of trust it is blind. Centralization is perfect blind trust. 

If there is no such trust, things are more complicated. That's why we have blockchain, which providers decentralized trust between parties. That's why dApps are running on blockchains. Blockchains use cryptography and consensus to gain trust between parties without a centralized root of trust. This sounds perfect with only one big cost: The performance is horrible compared with cloud computing applications. That is basically because of the two roots of trust: 

- Cryptography requires a huge amount of computation, limited by CPU power.
- Consensus requires network communication. Bandwidth is the ceiling.

There is huge progress in blockchain performance in recent years due to the improvement of the consensus algorithms, which can better utilize cryptography and network bandwidth. However, if compared with the user experiences of cloud computing, it is still far late behind.

## Adding hardware as the 3rd dimension to the 2 dimension blockchain world

To change the situation fundamentally, we may have to find another source of trust besides the existing 2. So we found the hardware root of trust. 
![root of trust of t-rust](https://cdn-images-1.medium.com/max/1120/1*5cLoCE4mLRw7hhDjcuaAxA.png)

Hardware root of trust is not something new. Trusted Computing technologies such as TPM chips have been used in all of our computers and most phones for years. Besides the cheap TPM chips, Intel and other CPU manufacturers have been using TEE as an enclave providing a trusted computing environment where you can safely run your code and data inside. 

Once we introduce the hardware root of trust as an additional dimension to our 2 dimensions world, things become much easier.

Because TEE (such as SGX from Intel) is centralized, there is no need to make a consensus on Intel's proof. Let's skip TEE technologies due to their centralized nature. Let's focus on Trusted Computing technologies (such as TPM only). Instead of making a consensus on cryptography results between all (or most) nodes across the whole network, making a consensus on Proof of Trust (PoT) data from hardware is much smaller and easier. 

## Can hardware lie?

However, here comes a big assumption that may or may not reliable. That is, the hardware can be trusted. If a TPM chip lies by providing the wrong PoT data, the consensus cannot detect or verify. As long as one of the roots of trust shaking, the whole top-level building collapsed too. This is the same concern as quantum computing may collapse existing cryptography, let alone the blockchain based on cryptography. So there will be the same answer: Yes, it can, but very hard.
Let alone the cheaper TPM chips, even expensive Intel SGX has been hacked. There is no way to build a 100% secure system unless you have an unlimited budget. So do hackers. Well, now the questions because can hardware secure enough that attackers cannot afford?

Now, the technical question converts to an economic question. How to increase the cost of attack while reducing the profit for a successful break-in. For more detail on this question, please refer to my previous blog 

> The first introduction video on TEA Project
https://pushbar.medium.com/the-first-introduction-video-on-tea-project-2b1da4eff6f1

and

> How we tried to break the TEA project, and why cannot https://pushbar.medium.com/how-we-tried-to-break-the-tea-project-and-why-cannot-938311b27848

Once you read (and watch) those two blog posts, you will get the answer.

## Can I run a TEA node on my existing computer?

Yes and No.

TEA node is nothing but a bunch of code running on a computer with TPM chips built-in. The hardest part is not to run it but to let others trust you. Before we invent the technology to verify other TEA Nodes running on all kinds of hardware platforms, we may limit the verifiable hardware among a few well-known trustable platforms. So you may either DIY a TEA node hardware using less expensive hardware components or buy from the market. This is not the best news but not the worst either. Because the consensus doesn't require complicated computation or huge bandwidth, even a super cheap single-board computing such as Raspberry Pi can run TEA Nodes. Currently, we are running our test environment on a RaspberryPi with a Nations Tech TPM chip. It works pretty well. Instead of running 100% useless hash in PoW blockchain, 99% of your miner's workload is spending on meaningful work. "Meaningful" here means profitable. You do not waste your electricity on PoW. Every dollar you invested makes money for you.

If TEA gets popular in the future, I believe many hardware manufacturers are producing compatible TEA node machines. Because we do not need all the IO ports (USB, Wifi, HDMI) and GPU on Raspberry Pi, each mining machine's cost would be meager. Possibly under $10. You can easily afford 100 or 1000 units on your TEA farm if you really into it. The more nodes you have, the higher profit you can get.
