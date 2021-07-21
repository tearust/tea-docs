# Challenges in TEA Token Economy Design
![money monkey](https://miro.medium.com/max/770/0*wHuoeWVaAxxfRVRU.png)



Token economy design is neither easier nor less important than technical design in a blockchain project. As a code monkey, I learned a lot about economics in recent years, but I still feel shaky when designing the TEA token economy. Thankfully, I got a lot of help from our community members such as "Blue Fox."
Today, I will talk about the challenges I was facing and how we plan to overcome them.

> You can skip the detail and jump to the last session **miners economy** of this article to learn "How TEA can cold start and make miners and all of us rich". 

## Roles in the TEA Ecosystem That Need to be Addressed

- **Miners (or farmers):** They buy or rent physical or virtual TEA mining machines. They earn reward from the execution of tasks the TEA consensus assigns to them. The reward are paid in T token, [//TEA] for short.
- **Camellia:** The name comes from the plant that tea is harvested from. In our TEA Project, Camellia is an NFT, CML for short. A TEA mining machine has to have an associated CML NFT to become an "active" mining node. CML can be traded as it has value. It also has a life cycle: it's born from a seed, grows into a tree, and eventually dies.
-**Investors (or landlords):** Investors don't want to deal with the hassle of maintaining a TEA mining machine. They are pure capitalists. They stake their [//TEA] to a Camellia owned by a miner. They receive revenue share in [//TEA] from this Camellia as a shareholder.
-**DAO:** The decentralized autonomous organization that governs the ecosystem. Think of it as a utopian-capitalist type of democratic government. Members vote using their staked [//TEA] to make decisions.
-**[//TEA]**: Last but not least, [//TEA] is not a role. It's a utility token with its value pegged to measurable computing consumption.

## The Challenges

- Incentives to miners to join the mining pool.
- The balance between investors and miners (landlords and farmers).
- The balance between new and old players. If old players rule, new players will walk away.
- The balance between the rich and poor. Maintaining a healthy balance will help prevent centralization over time.
- The balance between different types of TEA nodes to prevent centralization. Maintain a healthy diversity to prevent any single type of node dominating the system.
- The balance between long-term and short-term crypto investors.
- The balance between the core team and crypto investors.
- Population control.
- Avoiding pump and dump.
- Maintain the token's long-term value.

Although these are way beyond what a code-monkey is supposed to deal with,, as a crypto entrepreneur, these are issues I have to deal with. 

# T - the Stable Utility Token for Decentralized Trusted Computing
Miners need incentives to run nodes. $T is their reward.

![$T](https://miro.medium.com/max/563/0*Wd-1de7pQVidERlC.png)

When designing [//TEA], there are many options. Should it have a cap on total supply? Should it be a stable coin? If yes, what should it peg to? How to calculate the value? Should it be an asset or a currency? These are all important decisions that I have to make to ensure the health of the TEA Project token economy.

I did run through many versions. All of the previous versions had one or more problems. I finally balanced the pros and cons and selected the current version. I hope this is the last final version.

## A New Type of Stable Coin

[//TEA] is a stable coin pegged to the consumption of computing resources. Computing resources entails CPU instructions, RAM size, network traffic, storage, etc. Stable doesn’t mean it is stable compared to any fiat currency. Over time, computing costs will trend lower and lower, so the [//TEA] value should drop if measured against another fiat. However, for a specific computer task, the [//TEA] cost is stable. Whenever you run the same computing task, it will cost the same amount of [//TEA].
If the value of [//TEA] won’t rise, what’s the point for investors? Here's the trick. The investors won’t become wealthy just by holding [//TEA] without investing them in something else. Just as holding USD won’t make you rich, but investing USD in a startup company might if you choose wisely. Investors can invest their [//TEA] into Camellia, the most important concept in the TEA Project.

## Camellia, an NFT With a Life

![Camellia](https://miro.medium.com/max/550/0*yTaLtIQ38Sxfz2ZL.jpg)

Camellia, the plant that produces tea, is an NFT in the TEA ecosystem. Frankly, I drink tea but do not know too much about how tea was made. The only thing I know is that the Camellia plant can produce tea. That’s it. So I chose this name which I think makes sense.

Miners can setup a TEA node (the mining machine) on their own, but they still need Camellias to start mining. Camellia here is a kind of prerequisite for mining.

Camellia is an NFT. Every Camellia could be different somehow, such as classification, age, current owner, credit history, etc. All these properties define the outcome for this Camellia. For example, if it is too young or too old, it could not make as much tea as a mid-age Camellia. Some types of Camellia are less productive than others. Some types live longer than others. That’s why the price of Camellia may vary. Camellia itself is a big topic, we will talk about it more in the future. For now, let’s stick with the economics of [//TEA] for the rest of this article.

![TEA pegging](https://miro.medium.com/max/770/1*6IU3eufHmhzwyvBDqDx8YQ.png)

Unlike traditional cloud computing service providers, you cannot hire a specific miner to work for you for a set number of hours. No one knows which miner will be chosen to run your task. It's very important to keep zero-knowledge in order to prevent attacks. TEA consensus will choose a VRF miner to run your task. The TEA will measure the cost of computing as the "gas" fee. This is similar to Ethereum’s "gas" fee, so are the "tips." But TEA will be much cheaper compared to Ethereum’s gas cost because we do not need to run the same code on millions of nodes. We have a different way of consensus to get the trust.

## The Profitability of a Camellia and the Dispatching Algorithm

As a miner, you do not know and do not care what tasks are running in your node since you have no choice. What you can do is to get a higher chance to win some high-value tasks so that you can make more [//TEA]. The probability is the core algorithm of TEA PoT Consensus.

![Camellia life](https://miro.medium.com/max/770/1*U3m-XA-U_V-ENZ2wOGP2hQ.png)

In general, you can get a higher chance if your camellia is
- At a higher productivity age, e.g., at middle-age.
- A higher productivity type of plant, e.g., runs on more powerful hardware.
- Has a higher total stake value from investors staking on your node.
- Or some special features that others do not have, e.g., an onboard TPU.

All these properties are in the NFT definition. Such a high-outcome Camellia earns more [//TEA] for its owner, the miner and the stakeholders behind him. If the miner wants to sell it to someone else, they will probably fetch a high price for such a productive CML.

Assume the miner bought such a camellia from the seed when the price is inexpensive since a young camellia usually has a pretty meager expected outcome. If the miner sells it after it grows, the miners can earn a capital gain. This is one way to make an ROI.

## Stakes, Slots, and Investors

- Miners can invest [//TEA] to buy Camellia and sell at a higher price for ROI. How about the investors?
- Investors do not maintain TEA nodes but still make money from investing in Camellias.
- Each Camellia has a stack of "stake slots" that investors can stake their [//TEA] into. Similar to investing in a company, the investors are shareholders that earn dividends from the Camellia.

![Camellia staking](https://miro.medium.com/max/770/1*61gWwW3WsOzIWHX1bYYD6w.png)

The position of stake slots gives different "weights" when distributing revenue. The lower the index (near the bottom), the higher the weight. No doubt, when a new Camellia is born, the lowest open slot is first occupied by the fastest investor. By the way, the stake slot with index zero is dedicated to the miner himself. This is the only stake slot that cannot unstake unless the miner sells the Camellia. An investor can unstake their stake slots at any trading window. However, once unstaked, the upper slots will each slide down towards the open slot and then occupy a lower position. If the original miner wants to invest again in this particular Camellia, they can only stake the upper slots at the same price but receive less in weighted return. This design encourages investors to make long-term stake investments rather than short-term ones.

## Trading Window and Stake Slot Size

For ease of system design, we predefined the trading window and slot size. However, these numbers can be updated by the DAO or changed when the TEA mainnet starts. These are the placeholder numbers.
Each slot is worth 1000 [//TEA] (this number is subject to change before the mainnet launch) regardless of position. There is a trading window every 1000 blocks. For example, when the block height is 1000, 2000, 3000… n * 1000, investors can stake and unstake their slots at these blocks. Investors can only stake or unstake a full slot (1000 [//TEA]).

## Risks of Staking

As an investor, staking on a Camellia owned by a miner may cause a risk. The stake shares both revenue and risk. If the miner is a bad actor, he can run a malicious TEA node trying to cheat the system. Any random verifier can report this via Remote Attestation. Once the TEA consensus has confirmed this illegal behavior, the miner will get a penalty and all its stake will be burned. So before staking on a Camellia, make sure you search the miner’s credit history to control your risk.

We will talk about Camellia, which is more interesting than [//TEA] because it has life!

# Camellia, an NFT That Could Die
More or less you have probably known that TEA is a DAO of cloud computing miners (we sometimes call them farmers, TEA farmers) that run TEA nodes. TEA nodes work together to provide decentralized trusted computing services to traditional clients or modern blockchains. I explained [//TEA] token, the fuel (gas) of the TEA token economy earlier. Now I will explain Camellia, the soul of TEA nodes.

Camellia is the NFT that presents the soul of your TEA node. It describes what type of Camellia (hardware, software stack, versions), date of birth (how old it is), staking slots, and credit history (has it behaved poorly in the past). All of this information is stored and can be verified on the TEA layer-1 blockchain.
The Camellia NFT defines your TEA node’s productivity, life span, and most importantly, its value.

Let’s assume that "in real life", you're a farmer wanting to start a real tea business. You need to buy a Camellia seed and plant it in your farmland. If you do not own farmland, or your farmland is not big enough, you can rent land from a landlord. Your Camellia is not productive when it is very young. When it grows, it starts to make TEA for you. Different types of Camellia produce different types of tea. Of course, different kinds of tea have different prices. Your landlord shares some of your revenue.

Now let’s get back to our decentralized trusted computing business. Your node is your farmland. There are some investors who stake on you by purchasing your staking slots as mentioned earlier. You buy Camellia NFT seed and then plant it in your TEA node. Your TEA node is live now. It works with other TEA nodes and starts making revenue ([//TEA]). Of course, it is not very productive in the beginning. But after it grows up, it becomes more productive and generates larger amounts of revenue. Your stakeholders take some dividends as investors. When the Camellia gets older, its productivity drops. Eventually, it will reach the end of its life cycle and die. You will then need to buy a new Camellia seed and starts from the very beginning. You can trade the Camellia NFT in the exchange at any time just as your investors can trade staking slots.

You can see that the TEA token economy is exactly a mirror of real-life, and so it not surprising that Camellia will die just as everything living in real life does.

There are many benefits that derive from the fact that Camellia dies.

- New technologies bring new tech stacks on newer TEA nodes. Making old Camellia die can encourage miners (farmers) to update their hardware and provide better services. If Camellia never dies, the miners with an old machine can still make enough money due to accumulated credit scores over time. This gives them no incentive to upgrade.
- After old Camellia dies, miners need to buy new seeds to continue mining. The [//TEA] they spend on new seeds will be burnt by the DAO so as to maintain a healthy circulation of [//TEA].
- If old miners’ Camellia never dies, there will be less chance for newer miners to join and compete with old miners.
- Every new Camellia will bring in new staking slots that accept new investors (landlord) capital. This helps the capital flows and improves the overall ROI.

Imagine that people never die, what our human society will be like today?

# What is the TEA Project’s Investment Value Given the Camellia NFT Will Die and T is a Stable Token?

We've discussed earlier that Camellia is an NFT that dies. To put the CML and [//TEA] economy in context, let’s take a look at how our real-life economy runs.

The USD is a worldwide currency. Assume USD is a stable coin (although it's of course inflating faster and faster). You are not supposed to keep your USD bills in your vault and expect it to grow, right? Your only option to avoid the erosion of your USD value is to invest. Let’s say that you invest your USD capital in businesses. Every business in the market is an NFT. The business is born, grows, and eventually dies. Every business is unique. It has a different business model, different management team, and a different life span. If you invest in a blue-chip or early start-up, you will have different gains and risks. Rain or shine, most investors make more money compared to if they kept their money sleeping in their bank account.

Let’s turn back to the TEA economy. In the TEA economy, [//TEA] is USD. Holding [//TEA] in your Gluon wallet won’t make you wealthy. You'll need to invest. You can use your $T to buy Camellia seed and grow it. You can either make money from the [//TEA] generated from the Camellia mining or just simply sell it after it grows up. Remember that a young Camellia won’t be as productive as a grown one. So the price of Camellia will vary according to their age. Another choice would be to buy other miner’s staking slots. In this case, you gain the shared revenue from other miners. The revenue you receive varies because every Camellia is a different NFT, and every slot has a different “weight”. Finding the ideal slots to invest in is the key to your investment strategy. This is just like investing in a start-up or a blue-chip.

If you're smart and not too greedy, you can probably earn a lot from investing your [//TEA] in the TEA economy rather than selling them in the market. This helps “lock” the [//TEA] and maintaining a stable $T token price. Especially in the early stages of the TEA ecosystem.

There are a lot of detailed designs on the TEA token economy. I am trying to design an ideal token economy based on what I learn from economics.

# Mining Economy: How Will Miners Make Money? 
## Miners' Two Questions
If the TEA project was the Uber for cloud computing, miners would take the place of drivers. The incentive to the drivers is the fuel to drive the TEA token economy. Unlike centralized company who can pay salaries or own nodes, a carefully designed blockchain token economy can keep the project running and create speculation to boost growth. 

Rather than the big dream of the TEA project, the miners care mostly about ROI. Just two questions are important for miners:  
1. How many tokens can I mine given a particular investment (hardware, maintenance, time)?
2. Will the token pricing increase or at least maintain its value?

## Green  Mining? Or Rather, Green Farming!
Comparing with other crypto-mining projects, the TEA project is very "green." It doesn't burn huge amounts of energy with greedy processors, and it doesn't need to fill up hard drive space. It can run on small, inexpensive IoT machines. The mining hardware cost is therefor no longer a bottleneck for the TEA network. The majority of the cost comes from the Camellia NFT. 

## Positive Infinity Loop
For miners to get Camellia seeds, an auction is required, and miners must pay [//TEA] as currency. When new Camellia seeds are generated and sold through bidding, the DAO burns the TEA paid by the bidder. Because the supply of the seeds is heavily controlled and limited,  the price could increase sharply as long as more miners want to buy seeds. Miners want to purchase the seeds simply because mining [//TEA] is profitable, which means the [//TEA] price is high. The [//TEA] price is going higher because [//TEA] supply drops. [//TEA] supply drops because the DAO burns TEA, and the initial harvest mining outcome is low (Camellia needs time to grow). The DAO continues to burn [//TEA] because miners want to buy the seeds. This circulation becomes an infinity loop. As long as it can cold-start, it would run as expected. Now let's see how it starts.

## Cold Start
In the beginning, there are no [//TEA] tokens in the TEA blockchain. There are only frozen Camellia seeds (the NFT). Based on the logic settings, there are only a very few seeds that are defrosted at the beginning. They belong to the early investors. They start mining and harvest TEA at a relatively low outcome rate because the Camellia needs time to grow. The [//TEA] supply is minimal at this point, and all the [//TEA] owners are early investors. They are supposed to know the value of [//TEA] and Camellia. Otherwise, they won't invest in the TEA Project. Since they know, they are not likely to dump the [//TEA] in the market. Instead, they would invest their harvested [//TEA] to more staking slots and start more mining nodes to plant their Camellia seeds. The logic is that they can occupy the best staking slot positions, which become scarcer over a longer period. For example, if you got the insider message that a train station will be built somewhere, you would be well advised to buy the surrounding land before everyone else knows. If most of the early [//TEA] tokens are reinvested, there would be limited supply on the market. No doubt the [//TEA] price would go higher in such a scenario, not to mention the investors have tons of money to buy more [//TEA] tokens from the market.

Interestingly enough that if the [//TEA] price goes high, the more profitable [//TEA] farming becomes. If [//TEA] farming is profitable, more miners would like to start [//TEA] farming. But they first need [//TEA] to buy Camellia seeds. This is another market force pushing the [//TEA] price higher. 

## What if Someone Dumps?
Most of the early investors are rational and will reinvest. But there is no way to prevent someone from trying to dump [//TEA] into the market. In the early stage, the harvest outcome of [//TEA] is minimal. There won't be too much [//TEA] farmed and sold on the market. It would be much easier for the market maker to buy [//TEA] and keep the price healthy. As long as the price can keep at a healthy level and increase gradually, those who sold the TEA previously would regret their choice to dump [//TEA]. Therefore, the dump can be digested by the majority of miners.

## Leverage Existing IPFS Miners
Building a new community of miners is very hard. The TEA project won't create such a new community from scratch. Leveraging the existing communities is the key. The TEA project can bring value to them. For example, IPFS miners can merge mine FIL and TEA. TEA makes IPFS into "Interplanetary Function as a Service" rather than a pure file system. TEA dApps need code and data storage on IPFS, which brings a real use case to IPFS. Other smart contract platforms like DOT and ETH can offload their computing load to TEA. This offloading is not a diversion of their profit but creates more rich computing demands that are originally not doable in their blockchain. In return, more dApps run on their blockchain and generate more revenue. TEA is not trying to compete to or diverse profit from other partners, but to create new demand that benefits all.

## Eventually, the Demand and Usage of the T Token is the Key
No matter how well we design the miners' economy to boost [//TEA] initially, it's still a short-term solution. In the long run, the key rests in the demand for the usage of [//TEA] tokens. The TEA project team has started working on so-called rich dApps that run on the TEA network. Building the ecosystem, especially leveraging the existing FIL, ETH, and DOT ecosystem, is the team's main goal. The TEA Project team has started looking for cooperation with other major players to build the fusion ecosystem. One example is if we add the computing module to IPFS. IPFS miners can merge mine both FIL and TEA. The dApps also need to store data and code on IPFS, bringing more real use cases for IPFS. This is a win-win-win situation. 