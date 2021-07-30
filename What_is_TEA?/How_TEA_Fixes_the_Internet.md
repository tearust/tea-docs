# Decentralization is One of the Cures of the Current Internet Problem.

In [Decentralisation: the next big step for the world wide web](https://www.theguardian.com/technology/2018/sep/08/decentralisation-next-big-step-for-the-world-wide-web-dweb-data-internet-censorship-brewster-kahle), the author [Zoë Corbyn](https://www.theguardian.com/profile/zoe-corbyn) explained why. So I will focus on "how".

Whether you open a web browser or a mobile app, what you see running in front of you is just a client. The majority of the computational workload happens on remote servers. Developers write code, then upload it to some rented servers inside some giant data center. 

- You send your request to the server.
- The server runs the code and sends you back the response.
- The result eventually shows up on your screen. 

This is a typical request-response model. Even if you're chatting with a friend over an instant messaging app, the traffic is likely routed through a server somewhere in between. I wrote a blog post explain the 101 of cloud computing [here](https://medium.com/@pushbar/nste1-of-n-what-happened-after-you-click-a-submit-button-79f84b8c4f3e). It's a good primer if you're very new to Internet technologies.

In the current cloud computing model, trust is needed between developers, cloud service providers and the end client. Larger Internet service providers are usually considered more trustable than smaller companies. Especially when you're going to share some sensitive data, you usually double-check to see if the website you are using is the actual site and not an impostor. There are many phishing sites out there collecting user data illegally. But how do you know those brand names will not do evil? Well, speaking frankly, they do and always have. The Internet business model relies on monetizing user data. That's how the Internet giants make so much money by providing free services to their users. We'll discuss the [new business model](https://teaproject.org/#/doc_list/%2FWhat_is_TEA%3F%2Fhow_business_support_value.md) in the decentralized era in a separate article. Let's focus on trust for now.

Let's assume a common usage case:

- Your data is valuable and sensitive (e.g., your health data). 
- Your data needs some kind of computing power (data processing) to extract value from it. (e.g., a diagnostic algorithm or analytics).
- There are algorithms (code) created by developers that can do this job very well. You need to run the code with your data as input.
- The result is not only important to you, but also for others. For example, the code might involve COVID-19 analysis and contact tracing.
- However, you cannot run the code on your own. You do not trust the developers or service providers who host the code due to a concern about possible data breaches.

This is a typical problem the TEA Project is trying to solve. TEA's goal is to build a platform that allows code and data to runs inside trusted TEA modules without needing to trust anything else. The technologies built into the TEA platform protects the data and makes sure:

- The computation is based on the expected code and expected data. No one can alter the input code, the input data, nor the output result.
- The result of the computation is correct given the computing environment is verified.
- There's no data breach during the whole process.

TEA made this possible through the following factors:

- TEA nodes connect to each other through a peer-to-peer network.
- Every TEA node is protected and monitored by hardware TPM chips or the CPU's TEE (Trusted Execution Environment). The TPM can provide PoT (Proof of Trust). If utilizing the CPU, the CPU's TEE will rely on the manufacturer's verification.  
- Every TEA node can verify any other TEA node's integrity through a Remote Attestation process.
- The verification is controlled and determined by blockchain smart contracts. 
- Anyone outside the TEA module's hardware is ZK (Zero-Knowledge) about what happens inside the module. Neither the TEA node's owner nor the server connected to the module will know.
- Verifiable randomness makes it such that no one can predict which node is running or will run any particular task. This is also ZK.
- After the task is done, anyone can verify the workflow.
- A credit system and the token economy is enforced by blockchain smart contracts.

When a client deploys data to the TEA network to run on code provided by developers, nobody knows which TEA module will run the task in the future. The result will soon appear in the blockchain along with a series of PoT (Proof of Trust) data. Due to the token economy incentive, some others TEA nodes may have done the verification for you before the result appears on the blockchain. If you trust the blockchain, you can trust the result. You can also trust that no information was breached during the workflow because a zero-knowledge algorithm was applied to the task.


