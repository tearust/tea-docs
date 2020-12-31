# Where does the trust in T-rust come from?

If you haven't read my previous blogs about the Tea Project and T-rust framework, let me briefly introduce the relationship between these two concepts.

The TEA Project was created by a team of developers building a decentralized framework and applications based on trusted computing and blockchain. 

T-rust is the name of the framework that applications can run on top of. Because T-rust is so far (and will most likely continue to be) the only framework used in the TEA project, sometimes we say that TEA refers to T-rust, so all of the following statements are valid:

- I am a TEA project developer.
- Gluon and T-rust are two TEA projects.
- Gluon is a TEA application.
- My application is running on TEA. 
- My application is running on T-rust.

Gluon is the first application we built on top of T-rust (except for the first demo app which runs Tensorflow AI on blockchain). We are confident that there will be more applications running on top of T-rust in the future, but why would developers want their applications running on top of TEA rather than directly on top of blockchain or a cloud-computing server?

## Why not run applications on blockchain or the cloud?

If you don't intend for your application to be a decentralized app, it should be running on the cloud; it's cheap and fast. The only problem with that is that all 3 parties (developers, service providers, and clients) have to either ensure some kind of trust or not have trust at all. There are many ways to create external trust such as having developers hired by the company who use their code or using big service providers that you just know you can trust in general, but none of these can be guaranteed, so centralization is the perfect example of a process that requires blind trust.

But blind trust complicates things, hence the creation of blockchain which provides decentralized trust between parties. That's why dApps run on blockchains; they use cryptography and consensus to gain trust between parties without a centralized root. Everything sounds perfect, but there's a catch: The performance is horrible compared to cloud computing applications, this is caused by the two roots of trust: 

- Cryptography requires a huge amount of computation, limited by CPU power.
- Consensus requires network communication; the bandwidth becomes the ceiling.

There's been a huge progress in blockchain performance these past few years due to the improvement of consensus algorithms which allows for better utlization of cryptography and network bandwidth. However, if compared to the user experience with cloud computing, it is still far behind.

## Adding hardware as the 3rd dimension to the 2 dimension blockchain world

To address the situation, we may have to find another source of trust besides the existing ones, so we looked into hardware root of trust. 
![root of trust of t-rust](https://cdn-images-1.medium.com/max/1120/1*5cLoCE4mLRw7hhDjcuaAxA.png)

Hardware root of trust isn't new. Trusted computing technologies, such as TPM chips, have been used in all computers and most phones for years. Besides the cheap TPM chips, Intel and other CPU manufacturers have been using TEE as an enclave, providing a trusted computing environment where you can safely run your code and data. 

Once we introduce the hardware root of trust as an additional dimension to our 2 dimensions world, things become much easier.

Because TEE (similar to Intel's SGX) is centralized; there is no need to make a consensus on Intel's proof, so let's skip that option. Instead, let's focus on Trusted Computing technologies (such as TPM). Unlike making a consensus on cryptography results between most if not all nodes across the whole network, making a consensus on Proof of Trust (PoT) data from hardware is much smaller and easier. 

## Can hardware lie?

A common misconception is that hardware can be fully trusted. If a TPM chip lies by providing the wrong PoT data, the consensus cannot detect or verify anything. As long as one of the roots of trust shakes, the upper half of the pyramid will collapse too. This is the same concern as with quantum computing which can collapse existing cryptography, making blockchain based on cryptography even more vulnerable. So the answer is yes, but it can be very hard to do so.

This is even more evident with cheaper TPM chips (even expensive Intel SGX has been hacked). There is no way to build a system that is 100% secure unless you have an unlimited budget, so here's the real question: is hardware secure enough for most attackers not to afford hacking into it?

While this is more of a technical quesion, we can also look at it from an economic perspective; how do we increase the cost of attacking while reducing the profit of a successful break-in? If you're interested to know, checkout my previous blog.

> The first introduction video on TEA Project
https://pushbar.medium.com/the-first-introduction-video-on-tea-project-2b1da4eff6f1

and

> How we tried to break the TEA project, and why cannot https://pushbar.medium.com/how-we-tried-to-break-the-tea-project-and-why-cannot-938311b27848

## Can I run a TEA node on my existing computer?

Yes, but also no.

A TEA node is nothing but a bunch of code running on a computer with TPM chips built-in. The hardest part is not running it, but assuring others that they can trust you. Before we invented the technology to verify other TEA Nodes running on all kinds of hardware platforms, we were limited to using verifiable hardware made by the few, well-known, trustable platforms out there, so you may either create DIY TEA node hardware using less expensive components or buy them pre-built from the market. This isn't the best news, but not the worst either. Since the consensus doesn't require complicated computation or a huge bandwidth, even cheap single-board computing such as Raspberry Pi can run TEA Nodes. 

Currently, we are running our test environment on RaspberryPi with a Nations Tech TPM chip. It works pretty well. Instead of running useless hash on PoW blockchain, 99% of your miner's workload will be spent on meaningful work. And by meaningful, I mean profitable. You don't need to waste your electricity on PoW anymore; every dollar you invest will make money for you.

If ever TEA succeeds in the future, I believe many hardware manufacturers will produce TEA node compatible machines. Because we don't need IO ports (USB, Wifi, HDMI) and GPU on Raspberry Pi, mining machines will cost less (possibly under $10). You can easily afford 100 or 1000 units in your TEA farm. The more nodes you have, the higher the profit.


