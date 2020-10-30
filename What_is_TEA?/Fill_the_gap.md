# Fill the gap between cloud apps and dApps

![title](https://miro.medium.com/max/980/1*AkzywcI13zucwat6AFcYQA.jpeg)

## The Decentralization Movement

Although still at an early stage, decentralization becomes a new movement for many tech pioneers and business investors.

During 2017–2018 Blockchain crypto hype, almost every day I heard many cool ideas about how traditional business applications will be turned decentralized to the blockchain world. Quite a few of them makes sense on marketing and business demand (although some others may not). Unfortunately, with the hype faded, those projects are (almost) all gone. So far, I can hardly find any of those ambitious ideas turned into a real application. I know there are many reasons, but one of the most important reasons in my mind is the technical difficulties. Any distributed system is hard, very hard to build. We have to face this and show our respect.

## Build dApp is very different than cloud apps

ETH could be the first blockchain project introduces the concept of dApps since the first (so far still the biggest) BTC project is not programmable. ETH opened a window of a new type of application — the smart contract. This could be the base of all other dApps, including TEA project too. However, if you already learned smart contract, you will soon understand that it is very far from the common business application.

Many so-called existing dApps just utilized a few smart contract features, but have to host on traditional cloud computing infrastructure. I would call this kind of dApps “Hybrid apps”. No matter how much they claim to be decentralized, it can be torn down by removing from the cloud host as dApps are supposed to be robust and disaster-resistant.

Why is that? Just because we do not have a decentralized computing infrastructure as we have had in cloud computing. Nowadays it is so easy and simple to deploy cloud services to Digital Ocean or Amazon, or use the CDN from Cloudflare or Fastly all over the world. We do not care how the complex cloud system works, or you need to do is to pay.

## Deploy and run your code/data in a decentralized manner as we currently do in cloud computing

What if we can build a similar “de”-cloud computing infrastructure that developer can just simple “deploy” and pay. His code or data will automatically run in a decentralized manner — No way to be torn down as cloud computing would — worry free!
This is how the idea of the TEA project come to my mind.

---

![](https://miro.medium.com/max/980/1*6Ckg5arUUuyM5VeMiFUn3A.jpeg)


When we design the TEA project, we try to fill the gap between dApps and Cloud Apps. At least we will try to make the developer reuse whatever they already know. Such as programming languages, tools, OS, even IDE. In most cases, you can still work as if you are still working with a server, though that was not true. Your code will not be running on a server. Instead, it will be running in many unknown and unpredict nodes. The reason we design unknown and unpredictable is to reinforce resilience and security. If Hackers know where your code/data located, it will become an easy target. However, as a developer, you do not care about this. What you will need to do is simply the following steps.

- Compile your server code to WebAssembly
- Using our deployment tools to deploy to the TEA network (based on IPFS)
- Do not forget to pay :)

Your code/data is encrypted first before saved to IPFS. Only trusted TEA nodes (passed remote attestation) have a copy of the decryption keys in their secured memory. The security of the TEA nodes is protected by hardware (TEE, TPM or HSM) and guaranteed by TEA consensus on Substrate Blockchain.

I listed quite a few concepts in my last long sentence. If you do not know all of them, let me give you a basic explanation here.

- Wasm: WebAssembly, a new ISA, bytecode binary format to executables
- IPFS: A decentralized file system.
- TEE, TPM or HSM: Trusted Computing technologies in chips or hardware enclosure
- Substrate: The tech base of popular Polkadot blockchain
- TEA: Trusted Execution and Attestation, the project I am talking about now

---
![](https://miro.medium.com/max/980/1*NC5GBbXHK8a86w3CClWkuw.jpeg)

You can use your existing programming languages, but you still need to compile to a new compiling target: Wasm. Not all existing code can be directly compiled to wasm and run, and not all languages can directly compile to wasm. Likely you may have to rewrite some business logic…well, still much easier than learning a new smart contract language. As far as I know today the languages can compile to wasm includes:

- .Net
- AssemblyScript
- C/C++/C#
- Go
- Java
- Javascript/TypeScript etc
- Kotlin
- PHP
- Perl
- Python
- Ruby
- Rust
- Swift

Full list of 37 languages clicks [this](https://github.com/appcypher/awesome-wasm-langs).

For your client-side app, you will need to make sure it can be load statically. For example, if your client-side app is a WebApp. Make sure compile it as static resources. It would be eventually loaded from IPFS as static files (js, HTML, CSS, jpg, etc.). NO SERVER is required!


In our milestone 1 demo, our client-side app is written in Vue.js. Our server-side code is written in Rust compiled to wasm with Tensorflow supports.

---
![](https://miro.medium.com/max/980/1*HvLadDuTXS8Ur-8zFXYmZQ.jpeg)

I have to mention although we try to allow you to reuse your existing tech stack, building a decentralized app is fundamentally different than a centralized app. Many concepts you may take for granted but not exists any more. For example, you are probably familiar with a database deployed in the server clusters to store all session data. Sorry, it is gone. We are still looking for a usable decentralized database solution. If you have any recommendation, please let us know. Your temp data store cannot be persistent because the node which runs your code is unpredicted and will be clean right after the task is completed (for security reason).

Generally speaking, the decentralized app runs slower than a centralized app. In return, you gain resilience, security, privacy and trust. Consider your app can never be torn down no matter how powerful your enemies are. No pain no gain, right?

## My dispassionate point of view on dApps

Even during the 2018 blockchain hype, I clearly talk to everyone my point of view on dApps: If an existing business logic runs well in a centralized way, there is NO need to convert to decentralized way. Only focus on the business logic should exist but has not existed due to lack of technologies before.

As I just mentioned, dApps usually run costly than traditional cloud apps. Unless there is a huge gain (privacy, national security, national defence, etc.), converting exists apps to dApps would be a bad idea. On the other side, if there is an opportunity that should exist to satisfy people demand, but not exist yet because we did not have the technologies to build until today. Lucky you, it is your opportunity!




