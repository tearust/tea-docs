# TEA Project
![s1](../res/s1.jpg)

TEA means Trusted Execution and Attestation. It happens to be one of the favorite drinks for many software developers. That's why coffee and tea are most commonly used as project names by developers, such as Java language, Coffeescript, Jasmine, Mocha, etc. 

In this blog post, we will discover
- What are the problems TEA is trying to solve
- How will TEA solve those problems
- What will TEA be used in the future

# Blockchain 3.0

![s1](../res/s2.jpg)

Blockchain has a short history starting about ten years ago. It can be split into three stages, commonly named Blockchain 1.0, 2.0, and upcoming 3.0.

The typical project of the blockchain 1.0 era is Bitcoin. This is the first time in human history that decentralized trust is established. This is a revolution. However, Bitcoin can only do plus and minus operations. Therefore what Bitcoin can do is just transfer funds between accounts. 

In the blockchain 2.0 era, the typical project is Ethereum (ETH). ETH made a huge step further by introducing smart contracts, much more than plus and minus. Smart contracts are a Turing complete virtual machine that can run relatively complex logic. That's why they are called contracts. 

Existing smart contracts are not perfect yet. Even simple logic may cost a lot, not only money but also time. As long as a contract needs a complex computation, it can hardly run on any blockchain 2.0 platform.
It is not uncommon that many contracts need to run complex computations based on big data or even AI. Currently, they cannot be handled. They need so-called blockchain 3.0. TEA project is one of the solutions. The core value of the TEA project is decentralized trust, complex computation, and big data. As long as those problems are solved, blockchain technologies could be widely used in many cases, which initially have to be handled by a centralized platform. This could be a huge change in human society.

# Computer and trust

![s3](../res/s3.jpg)
Building trust between computers is not a new problem. There are existing solutions in cryptographic algorithms, software technologies, and hardware technologies around this area since computers were invented. I listed a few in the picture, but there are more. While those technologies can solve a particular part of the problem, any single technology has significant limitations. Either make the computation super complex so that it cost more than benefit, or has known vulnerabilities can be broken-in. 

Cloud computing gets popular so that more and more data are centrally stored and processed in some central server. Those data becomes a big bait to hackers. As long as they break into one, they can get a massive return on investment. No doubt that more and more data breaches in recent years.

# Layered solution with token economy

![s4](../res/s4.jpg)
We believe there is no such single technology that can reach the balance between security and cost. The solution is to combine those technologies into a layered solution. The technology in each layer can leverage their most strength while minimizing their disadvantage by utilizing other layers' technologies. This solution could reach a sweet balance between cost, security, and performance. By leverage the blockchain's token economy, we turn the problem from "unable to break into" to "too expensive to break into." Users can set an affordable yet secure enough balance point between cost and security. The higher price you pay, the higher the security level you can get—Vice versa.

# Increase the attacker's cost while reducing their benefit
![](../res/s6.jpg)
The motivation of attackers is the return on investment (ROI). In the centralized computing (such as cloud computing) architect, although breaking in is very hard and costly, as long as they can break in once, the benefit is high enough to cover the cost. Not need to mention that they can easily break in other servers using the same technology because the marginal cost is getting lower.

To defeat the attacker's motivation, we can combine existing technologies to do two things:
- Increase the cost of attack attempts
- Decrease the benefit of a successful attack

Once a successful attack's benefit is lower than the total cost of attack attempts, there is a negative ROI to the attackers. They either give up or turn to other low hanging food.

Here is the TEA project's main point; We combine existing technologies into a multi-layer solution to get a perfect balance between cost, security, and performance. This idea is exactly how blockchain builds decentralized trust. For example, Hacking the Bitcoin ledger is technically doable but economically not possible due to the cost. Bitcoin has been running for more than ten years. Everything in Bitcoin is open-sourced. Everyone knows how to modify the bitcoin ledger but never be done. The beauty of blockchain consensus and token economy.

When data stored in a single known location, it becomes a big bait to hackers. If we distribute the data into many different nodes (we used IPFS with small modification), each site owns a small portion of the data and is protected by different technologies. Attackers have to get all or most of the data pieces to make it useful. This will significantly increase the attacking cost since the marginal cost is high. Even the attackers can hack into one location to get a small portion of valuable data. This small portion is protected by cryptography and worth nothing unless combine with other pieces. Attackers still have to spend the same or maybe higher cost to break into other locations or all locations to make the data valuable. Not to mention by using the Zero-Knowledge algorithm, the attackers have no way to know if their current target is worthwhile or just a phishing bait. The risk, cost, and benefit are not predictable. This can hugely defeat the attackers' motivation.

In this picture, we listed the technologies we used in the TEA Project. We will go through them in the following slides. 

# Three chains technical architect

![](../res/s7.jpg)
We group the technologies into three categories. We call them three chains: 

- Blockchain
- Trust chain
- Delegation chain

In the TEA project, the root-of-trust (RoT) comes from two dimensions: Hardware root of trust (Hardware RoT) and software root of trust (Software RoT). The hardware RoT can be TPM of Trusted Computing Technology or CPU TEE. The software RoT is blockchain.

We leverage blockchain's immutability to do two things. 
- Store the important trust data. Once they are saved, there is no way to modify
- Smart contracts to run governance and consensus. Token economy happens here

One thing needs to mention. The blockchain in the TEA project doesn't make a consensus on the result of the computing result. Instead, it makes a consensus on PoT (Proof of Trust) to all involved nodes to ensure the whole workflow and execution environment is secure. The blockchain itself won't touch or store any secrets. 

The trust chain definition as quoted from Wikipedia:
 "In computer security, a chain of trust is established by validating each component of hardware and software from the end entity up to the root certificate." It is intended to ensure that only trusted software and hardware can be used while still retaining flexibility. In the TEA project, the root of trust can only come from hardware. Currently, we accept TPM or CPU TEE as the hardware root of trust (RoT). We knew that even the hardware RoT has vulnerabilities, but by combine the hardware trust chain with blockchain and delegation chain, the risk is minimized to be acceptable.

The hardware root of trust (RoT) generate proof of trust (PoT) data at runtime. The PoT data is stored and evaluated by random remote verifiers using blockchain consensus. The randomness of the remote verifiers is guaranteed by both blockchain and delegation chain. The randomness can be verified too.

The delegation chain is a network protocol. It guarantees that all the secrets to being kept inside and transferred between verified trusted hardware only. The protocol also maintains verifiable randomness when distributing the data to their hosting (we call it Pin and Repin). The whole data distribution flow can be traced by a series of signature chained together. That's why it is called a delegation chain. With the same blockchain methodology, altering the traceable delegation chain data is hard once the chain is set. Due to the randomness and zero-knowledge nature, no one, including the node's owner, cannot control and won't know what a node is currently running or about to run. The randomness and zero-knowledge increased the risk and cost of potential attackers. The traceable delegation chain records will be released to the blockchain after the computation is completed. At that moment, all the data has been wiped out. Attacking is useless.

# Four technical pillars of TEA project



![](../res/s8.jpg)








