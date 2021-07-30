# Turn IPFS (File System) into a new IPFS (Function as a Service) by adding some TEA

IPFS is awesome! It allows you to store your code or data in the middle of nowhere. When you need them, you can get it from somewhere you don't really care about. You can verify the hash to make sure this is exactly what you requested. How cool is that!

However, it's just a file system so far. If you need to run your code, you probably have to load the code from IPFS to some centralized cloud services first (Amazon, Google, etc.) If you could run your code directly in an IPFS node, you could get the result directly and saved your code a side trip to computing servers. You don't really need the code; what you need is the result, right?

# How do I know the result is correct?

If you were getting a piece of data from IPFS, you don't worry too much about the correctness of the result. You can easily verify the result by hashing it and the CID should match. But if you get a result of a computation of a piece of code and a piece of data, you don't know the result yet, not to mention the hash of the result. How do you verify?

# A quick answer: you don't

Since you don't know the hash of the correct result, you cannot verify using the traditional way, and you don't need to. What you can verify is the Proof of Trust (we call it PoT, Tea-Pot). The PoT is simply a series of valid proof of how your code or data is processed in the T-rust network. The math and silicon physics protects the computation process so that as long as you can verify the PoT, you can trust the correctness of the result.

BTW, if you are new to my channel, T-rust is a d-App platform built by the TEA project team. To learn more about TEA and T-rust, visit the https://teaproject.org website and try the demo.

# How does it work? Basically?

A typical IPFS network with four nodes works like this:

![](../res/blog/1_InPKDAJtmsKjLhT7HyfW8A.png)

The illustration simplifies IPFS but this will make the explanation easier.

Now we add a "TEA module" to some IPFS nodes (In the diagram below, all nodes have a TEA module, but they don't have to).

![](../res/blog/1_gSQnUb64RiS6nnH1U6h4ZQ.png)

The TEA module is a small cheap computing unit with a TPM chip built-in. In our demo, we used a Raspberry Pi Single Board Computer ($30) plugged with a Nation Technologies TPM Chip (unknown price, it should be $1 or so). In theory, any circuit board with CPU and TPM works, such as Nano Pi which I think may work better than Raspberry Pi.

The TEA module connects to IPFS only. It relies on IPFS and LibP2P to provide storage and network. TEA modules connect to other TEA modules using a secured connection (security keys protected by TPM hardware) forming a layer-2 network. Although physically, all information between TEA modules needs to go through the IPFS network, and the communication is worry-free due to hardware encryption.

![](../res/blog/1_AlcMa8MEW_D-xr9Mr_yk5Q.png)

All computational work including decryptions are processed inside the hardware-protected secure module. The TPM monitors the entire hardware even before the system boots. All the critical security evidence is stored in TPM as PoT. The PoT will be sent to layer-1 blockchain for Remote Attestation by other VRF selected "known good" TEA nodes. The consensus is done at the blockchain layer (we call the blockchain layer layer-1). The clients only need to query the layer-1 blockchain to verify the PoT is posted in a valid block so that they can trust the correctness of the computing result. Sorry about the long sentences in this paragraph. Let’s break them down into human language.


# Discover the TEA module

![](../res/blog/1_hUAugsefJtWmAL3noiEQKA.png)

These are the logic blocks of a TEA module. The red "secure zone" is running inside the protected area. In our demo case, it is a raspberry pi single board computing with a Nations Technologies TPM chip plugged in. The green "non-secure zone" is outside of the Raspberry Pi. It could be inside your IPFS node or standalone server as long as they are all in the same LAN. Because they are non-secure, all sensitive data has been encrypted before entering this area, and no additional protection needed.

If you're new to blockchain or trusted computing, you could be confused by those new terms in the diagram. Because we will only focus on IPFS in this blog post, I would recommend you to read the documents of the TEA project to get some background knowledge. Here is the [link to trusted computing](https://teaproject.org/#/doc_list/%2FWhat_is_TEA%3F%2FTEA_vs_Trusted_Computing.md) and the [link to the blockchain](https://teaproject.org/#/doc_list/%2FWhat_is_TEA%3F%2FTEA_vs_Blockchain.md).

# Do you mean I can store encrypted data in IPFS with TEA’s help?

Yes! There's much more than saving encrypted data to IPFS and keeping the key in your pocket. Your key can be protected by and transferred between TEA modules. You can define who, when, and how the key is to be used using the logic defined in your dApp (blockchain smart contracts will also work). Only those who meet the predefined conditions can unlock your data and consume it.

Since you can define the condition, you could write the logic like:

- Pay $1 every time someone uses your data.
- Only allow loading when code is running inside a protected secure zone.
- Only allow loading by TEA nodes listed in an whitelist, or block in a blacklist.
- Expire after a specific expiration date.
- Run for free for the first 10 times as new users. After that, charge $2 every hour.

There's many kinds of business logic that can be achieved here.

You can see how TEA not only protects your data but also makes your data *profitable!*

[[Repin]]

There are financial motivations behind the process. For more on the business model please [read this document](https://teaproject.org/#/doc_list/%2FWhat_is_TEA%3F%2Fhow_business_support_value.md).

Those pinner TEA modules actually have a copy of K1 in their secure memory, and the D1 in IPFS. So long as someone needs to consume D1, it can easily use IPFS DHT Findprov deployment_id to find who the pinners are. Those pinners would become the executor in the next step.

# Run the code securely in an executor protected by TEA

From now on, we separate the usage of code and data. Although code is also data from a storage point of view, code can execute as a function but data can become the parameter of this function.

Let’s assume both code and data have been deployed and repinned by many TEA modules. When someone (the client) pays to run the code against the data, he creates a task. In the TEA project, we call those small tasks "errands" because they are just function calls. The client posts the errand and payment to the layer-1 blockchain. All the existing pinners will receive the event from layer-1. They compete to get a chance to run this errand. The winner (executor) will get the money from the client. But not alone, as there are other roles to share which I will explain in a minute.

![](../res/blog/1_gZX1aB2NTFlYSoRsKOXIgw.png)

The competition is a complex algorithm we call “Delegation chain” in the TEA project. For the detail on the delegation chain please [read this document](https://teaproject.org/#/doc_list/%2FUnder_the_hood%2FDelegation_chain.md) on the Teaproject.org website.

The delegation chain algorithm can find the best suitable executor using the VRF algorithm from those competitors and a group of verifiers. The verifiers do not run the code, but run remote attestation on the executor to make sure it doesn’t try any monkey business. After the execution is completed, the encrypted result along with those PoT from verifiers are sent to the layer-1 blockchain. After the blockchain reaches consensus, a confirmation will be posted in a new block. Because the blockchain we're using (Substrate from Polkadot) is deterministic, the result is confirmed at this moment. The client can verify the new block's PoT and trust the result's correctness.

All the executor, verified, and delegators will share the revenue based on predefined business logic. They deserve the profit because of their hard work and luck.

# Using IPFS — Inter Planetary Function-as-a-Service

So far we only allow functions compiled to WebAssembly to be called due to security reasons. Besides this, anyone can use T-rust's trusted computing services as long as the client paid the deposit in layer-1 and called the T-rust API.

Among all of the possible clients, the blockchain oracle is the ideal use case that we're currently working on.

Due to the nature of blockchain consensus, running complex logic in smart contracts is very hard and expensive. Our T-rust can take over our client’s blockchain’s expensive computation so that our client blockchain can off-load then focus on the financial-related consensus. This kind of workload shifting is usually called a "computational oracle".

![](../res/blog/1_-uokQfRHLaCahX7l3awolg.png)

When the smart contract calls a layer-2 function, the off-chain worker will take over the call as an RPC. Because the call is async, the result won’t be inserted into the current block. The RPC goes to the T-rust network. After a few seconds, the result shows in T-rust layer-1 with the PoT ready. Multiple client off-chain workers get the notification from T-rust. After their verification (on PoT), they sign a result-transaction back to the client blockchain. As long as more the 2/3 designated off-chain workers agree on the result, the result is put into the next block. The smart contract continues running with the result as input.

# Talk is cheap, show me your demo!

Our current demo is a Tensorflow image recognization algorithm in wasm. If you go to our demo page https://teaproject.org/#/demo and follow the step by step instructions, you can try to run the pre-deployed demo. Furthermore, you can deploy any image or replace the preset Tensorflow code with your own. For more experienced users, it'll be more challenging to download the docker-compose.yml file and run your TEA module simulator yourself. You can even be a miner to try to mine some tokens yourself by providing services to others!

# The stage of the TEA project

While you're reading, you're probably already aware that the TEA project is a huge and ambitious project. If you read my previous blog post, you can get the background and the mission of this project. As I mentioned on the project home page:

![](../res/blog/1_y_yhcdh9XQl6AOjDmEGsmg.png)

We have been coding for our first milestone for about a year now. We're still at a very early stage. We're approaching the first fundraising stage (as of today, Nov 2020). We currently have 4 developers working on this project. I hope the funding can help us to get more team members to join us full-time. The business model can be found [here](http://t-rust.org/#/doc_list/Business_model%2FREADME.md).

![](../res/blog/1_7bsOjdvO4J2IbhETMxPtAg.png)

I call it a double loop. Basically, investors can invest in crypto NFTs (non-fungible tokens) but gain profit in fiat (service fees). When the NFT price goes up, investors can sell the NFT for crypto in return. We won’t provide an exchange channel between crypto and fiat, the two loops are totally separated.

Every NFT is the identity of a physical TEA module. It has a life cycle like everything in our universe.

![](../res/blog/1_geYaelG6PNV-jaEZCdj7zg.png)

The life cycle design keeps a healthy balance between old existing nodes with newborn nodes. This helps ensure that everyone has an equal chance to win in this game.
