# Challenges in TEA token economy design
![money monkey](https://miro.medium.com/max/770/0*wHuoeWVaAxxfRVRU.png)



Token economy design is neither easier nor less important than technical design in a blockchain project. As a code monkey, I learned a lot about economics in recent years, but I still feel shaky when designing the TEA token economy. Thankfuly, I got a lot of help from our community members such as "Blue Fox."
Today, I will talk about the challenges I was facing and how we plan to overcome them.

> You can skip the detail and jump to the last session **miners economy** of this article to learn "How TEA can cold start and make miners and all of us rich". 

## Roles in the TEA Ecosystem that need to deal with

- **Miners (or farmers):** They buy or rent physical or virtual TEA mining machines. They earn reward from the execution of tasks the TEA consensus assign to them. The reward is paid in TEA token, $T for short.
- **Camellia: The name comes from the plant that tea harvests from. In our TEA Project, Camellia is an NFT, CML for short. A TEA mining machine has to have a CML associate to become an “active” mining node. CML can be traded as it has value. It also has its life cycle. It was born from seed. It grows and eventually dies.
Investors(or landlords): They do not want to deal with the hassle of maintaining a TEA mining machine. They are pure capitalists. They stake their $T to a Camellia owned by a miner. They receive revenue share in $T from this camellia as a shareholder.
DAO: The decentralized autonomous organization that governs the ecosystem. Assume it is a Utopian-Capitalism-type democracy government. Members vote using their stake to make decisions.
Last but not least, $T is not a role. It is a utility token. Its value is pegged to measurable computing consumption.

## The challenges

- The incentive to miners to join the mining pool
- The balance between investors and miners (landlords and farmers)
- The balance between new and old players. If old players rule, new players will walk away.
- The balance between the rich and pool. Maintain a healthy ratio to prevent centralization over time.
- The balance between different types of TEA nodes to prevent centralization. Maintain a healthy diversity to prevent any single type of node dominates the system.
- The balance between long term and short term crypto investors
- The balance between the core team and crypto investors
- Population control
- Avoid pump and dump
- Maintain token long-term value….

Do you think these are way beyond what a code-monkey is supposed to deal with? Well, that’s true. However, as a crypto entrepreneur, I have to deal with them. 

# $T: the stable utility token for decentralized trusted computing
Miners need incentives to run nodes. $T is their reward.

![$T](https://miro.medium.com/max/563/0*Wd-1de7pQVidERlC.png)

When designing the $T, there are many options. Should it have a cap on total supply? Should it be a stable coin? If yes, what should it peg to? How to calculate the value? Should it be an asset or a currency? This is the most important decision I have to make first in the TEA Project token economy.
I did run through many versions. All of the previous versions have one or more problems. I finally balance the pros and cons, select the current version. I hope this is the last final version.

## A new type of stable coin

$T is a stable coin pegging to the consumption of computing resources. Computing resources mean CPU instructions, RAM size, network traffic, storage, etc. Stable doesn’t mean it is stable compare to any fiat currency. Over time, computing costs will be lower and lower, so the $T value should drop if measured by another fiat. However, for a specific computer task, the $T is stable. Whenever you run the same computing task, it will cost the same amount of $T.
If the value of $T won’t rise, what’s the point for investors. Here is the trick. The investors won’t be rich by holding the $T without investing them in something else. This is like holding USD won’t make you rich, but invest USD in a startup company may make you rich. Investors invest $T to Camellia, the most important concept in the TEA Project.

## Camellia, an NFT with a life

![Camellia](https://miro.medium.com/max/550/0*yTaLtIQ38Sxfz2ZL.jpg)

Camellia, the plant that produces tea, is an NFT in the TEA ecosystem. Frankly, I drink tea but do not know too much about how tea was made. The only thing I know is Camellia can produce tea. That’s it. So I use this name which I think makes sense.
Miners can setup a TEA node (the mining machine) on their own, but they still need Camellias to start mining. Camellia here is a kind of qualification of mining.
Camellia is an NFT. Every camellia could be different somehow, such as classification, age, current owner, credit history, etc. All these properties define the outcome of this camellia. For example, if it is too young or too old, it could not make as much tea as a mid-age camellia. Some types of camellia are less productive than others. Some types live longer than others. That’s why the price of Camellia may vary. Camellia itself is a big topic. We can talk in my future blogs. Please stay tunes. Let’s stick with $T in this blog.

![TEA pegging](https://miro.medium.com/max/770/1*6IU3eufHmhzwyvBDqDx8YQ.png)

Unlike traditional cloud computing service providers, you cannot hire a miner to work for you for 10 hours. You won’t know, no one knows, which miner will be chosen to run your task. This is very important to keep zero knowledge to prevent attacks. TEA consensus will choose a VRF miner to run your task. The TEA will measure the cost of computing as the “gas” fee. This is similar to Ehtereum’s “gas” fee, so are the “tips.” But TEA will be much cheaper than Ethereum’s cost because we do not need to run the same code on millions of nodes. We have a different way of consensus to get the trust.

## The profitability of a Camellia and the Dispatching Algorithm

As a miner, you do not know and do not care what tasks are running in your node since you have no choice. What you can do is to get a higher chance to win some high-value tasks so that you can make more $T. The probability is the core algorithm of TEA PoT Consensus.

![Camellia life](https://miro.medium.com/max/770/1*U3m-XA-U_V-ENZ2wOGP2hQ.png)

In general, you can get a higher chance if your camellia is
- At a higher productivity age, e.g., at mid-age
- A higher productivity type of plant, e.g., a more powerful hardware
- Higher total stake value from investors behind you.
- Or some special features that others do not have, e.g., onboard TPU

All these properties are in the NFT definition. Such a high outcome camellia earns more $T for its owner, the miner and the stakeholders behind him. If the miner wants to sell it to someone else, of course, the price could be high.

Assume the miner bought such a camellia from the seed when the price is meager because a young camellia usually has a pretty low outcome. If the miner sells it after it grows, the miners can earn the capital gain. This is one way to make an ROI.

## Stake slots and investors

Miners can invest $T to buy camellia and sell at a higher price for ROI. How about the investors?
Investors do not maintain TEA nodes but still make money from investing in camellias.
Each camellia has a stack of “stake slots” that investors can stake their $T into. Similar to investing in a company, the investors are shareholders. They earn dividends from the camellia.

![Camellia staking](https://miro.medium.com/max/770/1*61gWwW3WsOzIWHX1bYYD6w.png)

The position of stake slots means different “weights” when distributing revenue. The lower the index (near the bottom), the higher weight. No doubt, when a new camellia is born, the lowest open slot is first occupied by the fastest investor. By the way, the stake slot with index zero is dedicated to the miner himself. This is the only stake slot that cannot unstake unless the miner sells the camellia. An investor can unstake their stake slots at any trading window. However, once unstake, the upper slots occupy the open position. If he wants to invest again in this camellia, he can only stake the upper slots at the same price but much less weight. This design encourages the investors to make long-term stake investments rather than short-term ones.

## Trading window and stake slot size

To minimize the system design, we predefined the trading window and slot size. However, these numbers can be updated by DAO or changed when the TEA main net starts. These are the placeholder numbers.
Each slot worth $T1000 (this number is subject to change before the mainnet launch) regardless of the position. There is a trading window every 1000 blocks. For example, when the block height is 1000, 2000, 3000… n*1000, the investors can stake and unstake the slot at these blocks. Investors can only stake or unstake a full slot ($T1000).

## Risk of staking

As an investor, staking on a camellia owned by a miner may cause a risk. The stake shares both revenue and risk. If the miner is a bad actor, he can run a malicious TEA node trying to cheat the system. Any random verifier can report this via Remote Attestation. Once the TEA consensus confirmed this illegal behavior, the miner will get a penalty up to burn all stakes. So before staking on a camellia, make sure you search this miner’s credit history to control your risk.

We will talk about Camellia, which is more interesting than $T because it has life!

# Camillia, an NFT that could die
More or less you have probably known that TEA is a DAO of cloud computing miners(we sometimes call them farmers, TEA farmers). They run TEA nodes. TEA nodes work together to provide decentralized trusted computing services to traditional clients or modern blockchains. I explained $T token, the fuel (gas) of the TEA token economy in my last blog. Today I will explain Camellia, the soul of TEA nodes.

any tasks and no incentive $T even if you run your dead TEA node for years.

Camellia is the NFT that presents the soul of your TEA node. It describes what type of Camellia (hardware, software stack, versions), date of birth (how old are you?), staking slots, and credit history (have you done anything stupid before?). All of this information is stored and can be verified on TEA-layer1 blockchain.
The Camellia NFT defines your TEA node’s productivity, life span, and the most important, value.

Let’s assume in real life, you are a farmer, you want to run a real tea business. You need to buy a camellia seed and plant it in your farmland. If you do not own farmland, or your farmland is not big enough, you can rent from a landlord. Your camellia is not productive when it is very young. When it grows it starts to make TEA for you. Different types of camellia produce different types of tea. Of course, different kinds of tea are different in price. Your landlord shares some of your revenue.

Now let’s get back to our decentralized trusted computing business. Your node is your farmland. There are some investors to stake on you by purchase your staking slots as I mentioned in previous blogs. You buy Camellia NFT seed and plant it in your TEA node. Your TEA node is live now. It works with other TEA nodes and starts making revenue ($T). Of course, it is not very productive in the beginning. But after it grows up, it makes a lot of revenue. Of course, your stakeholders take some dividends as investors. When the camellia gets older, productivity drops. Eventually, it will run to the end of life and death. You will need to buy a new camellia seed and starts from the very beginning. You can trade the Camellia NFT in the exchange at any time. Your investors can trade your staking slots too. The capital goes to the highest ROI.

You can see the TEA token economy is exactly a mirror of an economy in real-life. So you won’t be surprised that Camellia will die as all of us will.

There are many benefits that I design the Camellia to die.

- New technologies bring new tech stacks on newer TEA nodes. Make old camellia die can encourage miners(farmers) to update their hardware to provide better services. If Camellia never dies, the miners with an old machine can still make enough money due to accuminate credit scores over time. This makes them no incentive to upgrade.
- After old Camellia dies, miners need to buy new seeds to continue mining. The $T they spend on new seeds will be burnt by the DAO so that maintain a healthy circulation of $T.
- If old miners’ camellia never dies, there will be less chance for newer miners to join and compete with old miners.
- Every new camellia will bring in new staking slots that accept new investors (landlord) capital. This helps the capital flows and improves the overall ROI.

Imagine that people never die, what our human society will be like today?

# What is the TEA project’s investment value given Camellia NFT will die and TEA is a stable token?

I won’t be surprised that you would ask if you read my previous blog: Camellia, an NFA that dies.
Let’s see what our real-life economy runs.

The USD is a worldwide currency. Assume USD is a stable coin although it inflated faster and faster. You are not supposed to keep the USD bill in your vault and expect it to grow, right? What you are gonna do? Of course, to invest. Let’s see you invest your USD capital in businesses. Every business in the market is an NFT. The business born, grows, and eventually dies. Every business is unique. It has a different business model, different management team, different life span. If you invest in a blue-chip or early start-up, you will have different gains and risks. Rain or shine, most investors make more money than keep their money sleep in the bank account.

Let’s turn back to the TEA economy. $T is USD. Holding $T in your Gluon wallet won’t make you rich. You will need to invest. You can use your $T to buy Camellia seed and grow it. You can either make money from the $T generated from the Camellia mining or just simply sell it after it grows up. Remember the young camellia won’t be as productive as a grown one. So the price will be different by their age. Another choice is to buy other miner’s staking slots. In this case, you gain the shared revenue from other miners. Because every camellia is a different NFT, and every slot has a different “weight”. Find the ideal slots to invest is the key to your investment strategy. This is just like investing in a start-up or a blue-chip. All have their own pros and cons.

If you are smart and not too greedy, you can probably earn a lot from investing your $T in the TEA economy rather than sell them in the market. This helps “lock” the $T and maintain a stable $T token price. Especially in the early stage of the TEA eco-system.

There are a lot of detailed designs on the TEA token economy. I am trying to design an ideal token economy based on what I learn from economics.

# Mining economy: How all of us make money? 
## Miners' two questions
If the TEA project were Uber for cloud computing, miners are drivers. The incentive to the drivers is the fuel to drive the TEA token economy. Unlike centralized company can pay salaries or own those nodes, in the blockchain world, a carefully designed token economy can keep the system running and create speculation to boost growth. 

Rather than the big dream of the TEA project, what miners care about is just ROI. Just two questions from miners:  
How much tokens I can mine on a particular investment (hardware, maintenance, time)
Will the token pricing increase and maintain the value?

## Green mining? or no, green farming!
Comparing with other crypto-mining projects, the TEA project is very "green". It doesn't burn huge energy with greedy processors, and it doesn't need to fill up hard drive spaces. It can run on small, inexpensive IoT machines. So the hardware is no longer an issue and source of cost. The majority of the cost comes from the Camellia NFT. 

## Positive infinity loop
For miners to get camellia seeds, an auction is required, and miners must pay TEA as currency. When new camellia seeds are generated and sold through the bidding, the DAO burns the TEA paid by the bidder. Because the supply of the seeds is heavily controlled and limited,  the price could increase sharply as long as more miners want to buy seeds. Miners want to purchase the seeds simply because mining TEA is profitable, which means the TEA price is high. The TEA price is going high because TEA supply drops. TEA supply drops because DAO burns TEA, and the initial harvest outcome is low (Camellia needs time to grow). DAO burns TEA because miners want to buy the seeds. This circulation becomes an infinity loop. As long as it can cold-start, it would run as expected. Now let's see how it could start?

## Cold start
In the beginning, there are no TEA tokens in the TEA blockchain. There are only frozen Camellia seeds (the NFT). Based on the logic settings, there are only a very few seeds are defrosted at the beginning. They belong to the early investors. They start mining and harvest TEA at a relatively low outcome rate because the camellia needs time to grow. The TEA supply is minimal at this point, and all the TEA owners are early investors. They are supposed to know the value of TEA and Camellia. Otherwise, they won't invest in the TEA Project. Since they know, they are not likely to dump the TEA in the market. Instead, they would invest their harvest TEA to more staking slots and start more mining nodes to plant their camellia seeds. The logic is that they can occupy the best staking slots position, which is scarce over a long period. For example, if you got the insider message that a train station will be built somewhere, most likely, you will buy the surrounding land before everyone else knows. If most of the early TEA tokens are used in reinvest, there would be limited supply in the market. No doubt the TEA price will go high, not to mention the investors have tons of money to buy more TEA tokens from the market.

Interestingly enough that if the TEA price goes high, the more profitable for the TEA farming business. If the TEA farming is profitable, more miners would like to jump the TEA farming, but they need TEA to buy Camellia seeds. So the TEA price goes higher and higher. 

## What if someone dumps?
Even most of the early investors are rational and will reinvest. There is no way to prevent someone from trying to dump TEA in the market. As I mentioned above, at the early stage, the harvest outcome of TEA is minimal. There should not be too much TEA farmed and sold on the market. It would be much easier for the market maker to buy in the keep the price healthy. As long as the price can keep at a healthy level and increase gradually, those who sold the TEA previously would regret their irrational behavior. Therefore, the dump can be digested by the majority of miners.

## Leverage existing IPFS miners
Building a new miners community is very hard. The TEA project won't create such a new community from scratch. Leveraging the existing community is the key. The TEA project can bring value to them. For example, IPFS miners can merge mining the FIL and TEA. TEA makes IPFS into "Interplanetary Function as a Service" rather than a pure file system. TEA dApps need code and data storage on IPFS, which brings real use case to IPFS. Other smart contract platforms, DOT, ETH, can offload their computing load to TEA. This offloading is not a diversion of their profit but creates more rich computing demands that are originally not doable in their blockchain. In return, more dApps run on their blockchain generates more revenue. TEA is not trying to compete to or diverse profit from other partners, but to create new demands benefits all.

## Eventually, the demand and usage of TEA token is the key
No matter how well we design the miners' economy to boost the TEA initially, it is still a short-term solution. In the long run, the key is the demand for usage of TEA tokens. The TEA project team has started working on the so-called Rich dApps that run on TEA networks. Building the ecosystem, especially leveraging the existing FIL, ETH, DOT ecosystem, is the team's main goal. The TEA Project team has started looking for cooperation with other major players to build the fusion ecosystem. One example is if we add the computing module to the IPFS. The IPFS miners can merge mine both FIL and TEA. The dApps also need to store data and code on IPFS, bringing more real use cases for IPFS. This is a win-win-win situation. 