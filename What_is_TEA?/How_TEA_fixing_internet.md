# Decentralization is one of the cures of current internet problem.


In [Decentralisation: the next big step for the world wide web](https://www.theguardian.com/technology/2018/sep/08/decentralisation-next-big-step-for-the-world-wide-web-dweb-data-internet-censorship-brewster-kahle), the author [Zoë Corbyn](https://www.theguardian.com/profile/zoe-corbyn) explained why. So I will focus on "How".

No matter you open a web browser or a mobile app, what you can see running in front of you are just clients. The majority of the work loads actually happening on servers. Developer write code, then upload to some rental servers inside some giants data center buildings. You send your request to the server then server run the code, give you the response, finally show on your screen. This is a typical request-response model. Even you are chatting with you friend over an instant messaging app, the traffic most likely through a server somewhere in between. I wrote a blog post explain the 101 of cloud computing [here](https://medium.com/@pushbar/nste1-of-n-what-happened-after-you-click-a-submit-button-79f84b8c4f3e). You can read it in case that you are very new to internet technologies.

In the current cloud computing model, the trust is needed between developer, cloud service providers and client. Larger branding internet service providers usually more trustable then no-names. Especially when you are going to share some sensitive privacy, you usually double check if the website you are using is what you expected. There are so many phishing sites collect user data illegally. But how do you know those brand names do not do evil? Well, speak frankly, they do, and always do. The internet business model rely on user's data. What's why the internet giants make so much money by providing free services to their users. We will discuss the [new business model](New_business_models.md) in decentralized era in a separate article. Let's focus on trust for now.

Let's assume a common case:
- You data is valuable and sensitive (eg, your health data). 
- You data need some kind of computing (data processing) to make value of it. (eg. diagnostic algirhtm, or analysitcs)
- There are algorithm (code) developed by some developers. The code can do this job very well. You just need to run the code with your data as input.
- The result is not only important to you, but also for the others. Eg. COVID-19 analysis and distribution tracking.
- However, you cannot run the code on your own. You do not trust the developers, or any service providers who host the code due to information breaching concern.

This is a typical problem TEA is trying to solve. TEA's goal is build a platform called T-rust. It allows code and data runs in the TEA modules while no one need to trust any others. The technologies protect the data and make sure
- The computation is based on the expected code and expected data. No one can alter the input code and input data. Nor the output result.
- The result of the computation is correct. The computing environment can be verified.
- No data breaching during the whole process

TEA made this possible by the following factors
- TEA nodes connects to each other by a peer to peers network
- Every TEA node itself is protected and monitored by hardware TPM chips. The TPM can provider PoT (proof of trust). 
- Every TEA node can verify other TEA nodes integrity through a Remote Attestation process
- The verification is controlled and determinined by blockchain smart contracts. 
- Any one outside the TEA modules hardware is ZK (Zero Knowledge) about what happened inside. Even the TEA node's owner or the server connect to the module won't know.
- Verifiable Randomness makes no one can predict which node is running or will run what task. This is also ZK
- After the task is done, anyone can verify the workflow
- Credit system and Token economy enforeced by blockchain smart contracts.

When the client deploy the data to the T-rust, the developer deploy the code to the T-rust. They do not know which TEA module will run the task in the future. The result will soon appears in the blockchain along with a series PoT (proof of trust). Due to token economy incentive, some others TEA nodes have done the verification for you before the result appear on the blockchain. If you trust blockchain, you can trust the result. You can also trust no information breaching during the workflow because zero knowledge algorithm applied to the task.


