# Gist
TEA has two tokens. 

TEA: TEA, the ticker of the token, shortened as $T. It is a utility token. It is used for mining revenue and service fees (aka Gas in Ethereum). It is a stable token pegging to the measurable computing resources.

Camellia：Sometimes called "Tea Tree". It is the governance token in TEA DAO. It also represents the credit score and profitability of miners. Camellia has limited supply.  

In addition to the two tokens, there is another concept "Seed". Seed is not a token, but a qualification similiar to "head count". It is used to control the number of new miner nodes allowed to join TEA at any given time window. When there are more miners want to join, they need to obtain miner qualifications through bidding. Miners earn service fees TEA by executing customers’ computing tasks assigned by the system. In Ethereum and other blockchain, this concept is usually called Gas. The level of miners is represented by Camellia. The higher the Camellia, the higher the probability that the miner will obtain high-value computing tasks, and the higher the community responsibility and voting power. Inside DAO, Camellia is also considered an equity token, the owner can participate in tax dividends by locking up to. Camellia represents profitability so that it can also be used for the credit value of credit loans.


# Principles and Purposes of Economic System Design

- By introducing, we create an underlying support for Defi that supports under collateral lending
- Through the unmodifiable constitution and modifiable community governance, the interests of early participants and late participants are taken into account, so that the project can benefit from early investors while always maintaining metabolism for long-term development
- Create a legal utility token to avoid legal risks
- Automatically adjust liquidity, allowing speculation and investment to be controlled and profits coexist


# TEA: T$ Utility Token


## Generation and distribution of T$

TEA is the ticker of tokens, which can be abbreviated as T$. TEA is an Utility Token. It is similar to Ethereum's Gas. It is used to pay for the cost of executing client's computing tasks or the internal public services in the system. These costs include CPU usage, storage, and network traffic that is similar how the cloud computing measures costs. The genesis block will not include any TEA assigned to the team or early investors. All TEA needs to be obtained through mining.

## How to earn T$

There are several ways to earn T$

- Miners provide trusted computing services to earn gas fee and tips paid by clients
- Miners provide computing services for public services within TEA to obtain new minted TEA
- Anyone can purchase $T through token trade
- Any Camellia holder receives tax dividends through lock-up

## T$ issuance, total amount and price anchoring

Unlike Camellia, T$ has no limitation on total supply. Its inflation comes from the computational cost of public services. As long as there is computing resource consumption for public services across the network, an equivalent amount of $T will be issued to participants in public service mining. $T distributed is in proportion to the miners’ workload. It’s notable that customers pay $T for computing service provided by miner which is not part of minting of $T. 

As the network scale increases or decreases, the resource consumption of public services will also increase or decrease, therefore the inflation rate of TEA fluctuates along with the network scale change. When the economy improves, more miners join mining, the demands on public services increases, inflation rate will increase. On the contrary, when the economy deteriorates, the inflation rate will decrease.

Since public service will always exist, TEA will continuously inflate in the long run.

Since the pricing of computation is objectively measured based on the computational cost (such as CPU instructions, occupied time, network traffic or storage size and time, etc.), TEA is a stable currency pegging to computational costs.


## T$ price fluctuation and automatic market adjustment

Although TEA is a stable token that pegging to computational costs, when the market demand for computing tasks will also lead to price fluctuations caused by imbalances in supply and demand. For example, in the initial stage of TEA's launch, applications on TEA are underdeveloped and there are not many tasks needed to be executed. At this time, no one buys the TEA obtained by miners through public services. A large number of idle sell orders will result in a price drop. At this time, for traditional apps that originally used other centralized cloud computing, it may be found that the price is lower than the price of renting traditional cloud computing. , So as to purchase TEA computing services using TEA. This kind of payment will cause the price to rise until it is close to the computing price of traditional cloud computing. Another situation will push up the price of TEA. As mentioned below, based on security considerations, DAO will control Seed to avoid the sudden influx of a large number of miner nodes that are too late for security review to break the fault tolerance limit of BFT. Because the scale of miners is slowly growing, when the dApp on TEA is booming, a large number of computing tasks appear to be queued for processing. Customers need Increase the tip to get priority processing rights, so that the purchase order for TEA will increase, and the price will increase. As the price increases, more miners are willing to buy Seed to join the ranks of mining, thereby dispersing computing to release pressure and achieving the effect of reducing congestion. Then TEA The price of TEA will fall. Through this market mechanism for automatic adjustment, the price of TEA will fluctuate around the cost of computing resources.

In addition to adjustment of supply and demand by the market itself, there are various financial tools that can help prices return to stability, such as collateral lending, credit lending, future trade, etc.

## Public service rewards and distribution

Public services refer to node security review, block generation, code maintenance and system management costs for maintaining the system trustworthiness. These costs cannot find specific payer, and the beneficiaries are the entire community. Therefore, it is defined as public services. 

The costs of public service are allocated based on the computational consumption of these tasks through the new tokens generated in each block. In the early stage, it is mainly the block generation service and the computational resources consumed for security review. In the future, various DAO internal administration may be added. For example, if a node is selected for 100 security audits (Remote Attestation) on other nodes in the previous time period, it will receive the proportion of public service rewards generated at this stage based on consumed resources recorded by the billing system. This process is commonly known as mining.

Before $T can be purchased in the marketplace or provide computing services, mining is the only way to earn TEA.

## T$ trading, and ERC20 Lock&Mint, Burn&Redeem Protocol

T$ is a token based on Polkadot Substrate. It is not an ERC20 token issued on Ethereum. Therefore, it cannot be directly transferred to an ERC20 compatible wallet or exchange for trading. However, $T provides Lock&Mint and Burn&Redeem (LMBR) Protocol, which can be locked by TEA Network to get the 1:1 equivalent of ERC20 Token t.eth. This token is a standard ERC20 token and can be used for various financial transactions on any Defi system that supports ERC20. If the transaction is completed, you want to redeem the originally locked T$, you need to perform a Burn operation, and then the original $T token will be returned. There is no other financial loss except transaction fees. The same approach applies to other blockchains that support smart contracts and multi-signatures, such as Polkadot's t.dot token

## Various Defi businesses established on TEA in the future

TEA belongs to a basic blockchain service platform. In the future, with the development of the ecosystem, various Defi applications will be created on the platform. These Defi applications can directly use the trusted computing services provided by TEA, which support larger transaction volume and lower gas fee compared to traditional blockchains. Since these Defi appplications are built on TEA, they can be processed directly without ERC20 conversion. If you need to process external ERC20 compatible tokens, you can use the same Lock&Mint, Burn&Redeem protocol .

## Miner's cost

The cost of miners includes

- Purchase or rent  mining machine
- Electricity and network expenses
- Pay for the security audit

Because TEA uses trusted computing technology, miners need to bring their own or rent mining machines. In the initial stage, only Amazon Nitro trusted virtual machines are approved as mining machines. In the future, we will develop various types of mining machines that meet the requirement of risk diversification. 

These different architectures of mining machines include

- Google 基于 AMD Enclave 技术的虚拟矿机
- Microsoft 基于 Intel Enclave 技术的虚拟矿机
- These different architectures of mining machines include
- Independent hardware mining machine based on TPM

Google's virtual mining machine based on AMD Enclave technology
Microsoft's virtual mining machine based on Intel Enclave technology

Unlike POW consensus that requires a lot of computing power, TEA does not consume much power and doesn’t require super computing power. It belongs to the green mining type. Therefore, the expenses in this area can basically be ignored.

Because TEA requires uninterrupted, random and unavoidable security audits for all nodes that are eligible for computation, the machine may be audited as long as it is on standby mode. Auditing fee is required. If the node doesn’t pay an audit fee or audited failure, it will be considered as an unsafe node, thus it will be deprived of the qualification to participate in mining, and it will be fined, or even severely lost all Camellia and expelled from the network.

In the initial stage of network operation, the new T$ issued by the system with new blocks can cover these audit fees, therefore miners do not need to pay separately. However, as the number of nodes increases and the additional issuance of tokens reduces, this part of the cost will gradually shift to miners.

If the market deteriorates and the miner’s revenue is not enough to cover its daily expenses, the miner can choose to withdraw from mining. In this way, competition will decrease, and the income of individual miners will increase, thereby achieving the effect of automatically market adjustment. Once miners leave the system,  their original Seeds will be destroyed. The original Camellia can be transferred or sold to other miners. 

# Camellia

Camellia is an governance token inside the TEA network. It is introduced for the following purpose

As the basis for equity distribution, you can participate in the tax dividend after locking
Participate in DAO governance as a voting weight
As a reward for long-term honest provision of trusted computing services, it is also a punishment for violations and cheating
As credit collateral for excess lending

## Camellia is not a utility token

Camellia has no absolute numerical meaning which means a Camellia cannot peg to any entity value. This is different from the T$ peg calculation cost. Camellia only has a relative meaning. That is, the proportion of Camellia on your account to total Camellia, or the difference between your Camellia and your competitor's Camellia.

## Camellia issuance, the output decays with time and the total amount is constant

The number of Camellia contained in each block decreases according to the following calculation: starting from the genesis block, each block rewards 8 Camellia. Then after every 1M block, this number reduce to 80% of the previous value. According to 6 seconds block interval,  there will be 10 production cuts and the reward amount is less than 1 within 2 years. So far, the total number of Camellia is 37439440.37. Although the additional issuance will continue, when the number is small enough ( less than 10^-18)to be allocated to the miner's account, which is 0, additional issuance will be stopped.


## Camellia's lock-up status, equity income and taxes

Camellia has two states, one is the free state and the other is the lock-up state. Camellia in the free state does not obtain tax revenue dividends, nor can it be used to calculate the weight of computing tasks and the weight of voting.

In a free state, Camellia can circulate freely which means that it can be used as collateral or be sold.

In the lock-up state, Camellia is locked in the smart contract during promised time period. The owner gets a token certificate after the lock. During the lock-up period, the entire network tax will be distributed according to the proportion of this token certificate.

Tax will be introduced later.


## How to earn/lose Camellia

The principle of allocation of each block’s Camellia is

The more work, the more rewards. It has linear correlation with $T earned by miners
Square root of Camellia's proportion becomes the weight, which is used to mitigate the Mathew Effect (Rich get richer)
The calculation method is the absolute value of each miner’s own weight

```
weight_of_miner_i = tea_mined_by_miner_i_in_this_block * locked_camellia_of_miner_i.sqrt()
``` 
 
Miner's Camellia income

``` 
Camellia_income_for_miner_i = total_camellia_in_this_block * weigh_of_miner_i / total_weight_of_all_miners
```


From this formula, you can see that only $T obtained through mining is used to calculate weights, and those earned through transactions cannot be counted. This is to encourage miners to actively participate in the service, and the results are recognized by consensus. Camellia locked up by miners is distributed based on square root of proportion. Only the locked Camellia participates in the calculation. This is to encourage miners to lock up to drive Camellia price up. The reason for taking the square root instead of direct proportional distribution is to reduce the gap between the rich and the poor.

In addition to earning Camellia through mining, all users can also obtain Camellia through trading. Therefore, even if you are not a miner, you can still own Camellia, but those Camellia cannot distribute labor rewards. The main motivation for non-miners to own Camellia is tax income dividends and financial arbitrage.

Camellia, as a reward for miners' honesty and trustworthiness, is also used to penalize dishonesty and trustworthiness. When a miner commits malicious acts or improper operations that create an unsafe computing environment which is found out by a security audit and agreed that it is no longer secure and trustworthy, the miner will be penalized and even be kicked out from the system. This part of the Camellia will be allocated to the whistle blower and the arbitration node participating in the judgement, and the remaining part will be destroyed.

Because the total amount of Camellia has a limit, the inflation is decreasing. It can only be fined and destroyed without increasing indefinitely. The number of Camellia directly affects profitability. It is a scarce asset and has room for speculation.

## Camellia as voting weight

Only Camellia that is locked up can be used to calculate voting weights.

An important role of Camellia is voting power in DAO governance. While voting, Camellia is generated as a weight. Another role of Camellia is the weight that calculates the winning rate of task competition.

## Camellia's task allocation weight

Only Camellia in the locked up state rather than free state can be used to calculate the allocation weight.

In the consensus algorithm, the probability of a computing node being assigned to a task is proportional to the square root of the node's Camellia value. Designed as a non-linear ratio is to make up for the gap between rich and poor and class consolidation caused by the Matthew effect.

For tasks that have mandatory requirements for Camellia values, it is necessary to use the same method for random allocation within the range that meets the requirements. If requirements are too strict and there are few eligible nodes, the computation will cause security risks. We need to have a disclaimer of which users should take their own responsibilities and risks.

## Camellia's total turnover limit

为了避免女巫攻击, 也就是通过短时间聚集大量用户数和大量资金疯狂收购 Camellia 从而达到控制选举和共识机制的风险, 我们设置了全局 Camellia 转手限制. 如果前64 个区块总共发生了全网 Camellia 总额的 1/128的话, 这个区块讲不能打包任何涉及到 Camellia 转手的交易. 这些交易会顺延到下一个区块. 如果仍然超过, 就还是需要继续等待直到不再满足提交为止. 在交易不能达成期间 Camellia 仍然继续按照时间衰减, 所以交易的数额会在打包的时候重新计算或者取消.

In order to avoid witch attack, that is, to acquire Camellia frantically by gathering a large number of users and a large amount of funds in a short time to achieve the risk of controlling the election and consensus mechanism, we have set a global Camellia transfer limit. If a total of the first 64 blocks in the entire network produce 1/128 of total Camellia , this block cannot pack any transactions involving Camellia's transfer. These transactions will be postponed to the next block. If it is still exceeded, you still need to wait until the submission is no longer satisfied. When transactions are pending, Camellia will continue to decay according to time during the completion period, and the amount of the transactions will be recalculated or cancelled when packaging.

使用 Camellia 进行信用借贷 Use Camellia for credit lending
Camellia 可以认为是一种信用资产代表了对未来收入的预期. 高 Camellia 意味着高的未来 Gas 收入和更高的偿还能力. 因此 Camellia 可以用于超额借贷中的连带抵押物.
Camellia can be considered as a kind of credit asset that represents the expectation of future income. Higher Camellia means higher future gas income and higher repayment capability. Therefore, Camellia can be used as joint collateral in excess lending.

在 TEA 网络上的 Defi 应用可以把借款人的 Camellia 值作为是否发放贷款的参考依据. 根据借贷人的 Camellia 的数值可以制定合理的借款利率和不同的杠杆率. Camellia 不仅仅作为与其他抵押物一同作为信用参考值, 它自身也可以单独作为抵押物. 当借贷人无力偿贷的时候, Camellia 作为连带抵押物进行拍卖偿还贷款. Camellia 一旦作为抵押物, 放贷人就成为它的 Lien holder. 尽管从账号上看仍然属于原来的主人的账号上, 还可以继续用于各项 Camellia 的权益.
The Defi applications on the TEA network can use the borrower's Camellia value as a reference basis for issuing loans. According to the borrower's Camellia value, reasonable loan interest rates and different leverage ratios can be set. Camellia is not only used as a credit  reference with other collaterals, it can also be used as collateral alone. When the borrower is unable to repay the loan, Camellia is auctioned as a joint collateral to repay the loan. Once Camellia is used as collateral, the lender becomes its Lien holder even though the account still belongs to the original owner, and it can continue to be used for various Camellia rights.

Camellia 的破产拍卖交易Camellia's bankruptcy auction transaction
信用可以用于抵押物进行借贷. 那么在无法还贷的情况下就必须进行拍卖物抵押来偿还. Camellia 转手同样受到全网 Camellia 转手总额限制. 如果发生大量突发交易会自动拖延来避免女巫攻击来劫持投票和控制共识机制.
Credit can be used as collateral for loans. If the loan cannot be repaid, the collateral must be through auction. Camellia transfers are also subject to the total amount of Camellia transfers on the entire network. If a large number of unexpected transactions occur, they will automatically delay to avoid witch attacks and hijack voting and control the consensus mechanism.

Camellia 的增值空间假设Camellia's value increase hypothesis
早期的矿工由于竞争不激烈而且挖矿奖励高, 比较容易积累信用并相对于后来加入的新矿工具有权重上的优势, 所以更加容易获得任务积累财富. 但是随着活跃矿工增加以及产量降低, 计算任务分派概率和增发权重的时候都采用平方根的计算方式. 过于集中的 Camellia 并不会带来相应的高收益. 反而长久会造成社会分配区域平衡. 因此这时候是考虑卖出给新矿工获得投资收益. 这种方式有利于平衡新老矿工之间的利益, 促使项目可以长期发展.
In the early days, due to lack of competionierce, mining rewards were high, early miners were able to accumulate credit and had the advantage of being more powerful than the new mining tools added later, so it was easier to obtain tasks to accumulate wealth. But as active miners increased and output decreased, the probability of task assignment and the weight of additional issuance were calculated using the square root method. Camellia that is too concentrated will not bring corresponding high returns; it will cause the balance of the social distribution area for a long time. Therefore, this time, we are going to consider selling to new miners to obtain investment benefits. This method is conducive to balancing the interests of new and old miners, and promotes long-term development of the project.

税收和分红 Taxes and dividends
税收来源于每一个区块所有账号通过计算任务(无论是公共服务还是有偿客户计算任务)获得的 TEA 收益. 按照一个可以通过DAO 调节的税率来收取. 初始数值设定为 0.3%.
Taxes come from the TEA income obtained by all accounts in each block through computing tasks (whether public services or paid customer computing tasks). It is collected at a tax rate that can be adjusted through DAO. (The initial value is set to 0.3%)
这笔税收全部用于对锁定了 Camellia 的权益人按照锁定比例进行分发.
This tax is all used to distribute Camellia's stakeholders in accordance with the lock-up ratio


Seed 和计划生育 Seed and family planning:
目的
通过控制新节点涌入的速度来避免来不及进行安全审核, 尤其是新平台的安全审计存在漏洞带来的 BFT 共识容错底线被突破的风险. 在客观上也造成了一定程度的稀缺性. 为金融投机提供了可能性
By controlling the influx of new nodes to avoid too late for security audits, especially the risk of breaching the BFT consensus fault tolerance caused by loopholes in the security audit of the new platform. It also causes a certain degree of scarcity.

Seed 的数值计算系数 Birth_rate Seed coefficient Birth_rate
在任意一个给定时刻, 新区块里面允许增加的新矿工节点的数量叫做 Seed. 其计算方法是

Seed = math::round::ceil(total_Seed * (1 + birth_rate))
Seed numerical calculation coefficient Birth_rate
At any given moment, the number of new miner nodes allowed to be added in a new block is called Seed. The calculation method is shown below:

Seed = math::round::ceil(total_Seed * (1 + birth_rate))

在创始区块中有一个初始的 birth_rate, 未来可以通过一个算法来自动调节. 类似于 BTC 自动调节的难度系数. 不过 TEA 的出生率条件是根据任务拥塞程度来调节. 如果任务很少, 大量节点处于等待状态, 则说明市场不旺, 需要降低出生率避免恶性竞争. 如果任务很多, 甚至产生积压排队, 就需要提高出生率招募更多矿工来分摊任务和公共服务成本.

因为出块间隔比较短, 现在是 6s, 所以不是每个区块都允许有 Seed 的. 目前预计是每隔 128 个区块(约 12 分钟)Seed 个新矿工加入.

Seed 内部的多样性名额控制
为了防止女巫攻击, 以及过于集中的软件硬件架构造成不能及时发现的漏洞蔓延到超过 2/3 容错限制情况的发生. 在分配 Seed 的时候还需要额外遵循如下原则
There is an initial birth_rate in the founding block, which can be automatically adjusted by an algorithm in the future; similar to the difficulty coefficient of BTC automatic adjustment. However, the birth rate condition of TEA is adjusted according to the degree of task congestion. If there are few tasks, a large number of nodes are in the waiting state, meaning that the market is not prosperous and the birth rate needs to be reduced to avoid vicious competition. If there are many tasks, it is necessary to increase the birth rate in order to recruit more miners to share the cost of tasks and public services.

Because the block interval is relatively short, (it is now 6s) not every block is allowed to have Seed. It is currently estimated that new Seed miners will join every 128 blocks (about 12 minutes).

Diversity quota control within Seed
In order to prevent sybil attacks and over-concentrated software and hardware architectures, vulnerabilities that cannot be discovered in time spread to more than 2/3 of the fault tolerance limit. The following principles need to be additionally followed when allocating seeds.

任何一种软件硬件结构的矿机在超过 1/3 数量的时候开始受到价格控制. 也即是说需要支付更高的 Seed 购买费用来获得 Seed
任何一种软件硬件结构的矿机在超过 1/2 数量的时候就停止发放新的 Seed, 直到比例低于 1/2 才可以恢复
这种比例控制方式有助于全网软硬件结构的多样化. 避免发生一个漏洞可以攻陷超过 2/3 节点的情况

获得 Seed 的竞争
当有超过 Seed 数量的矿工希望加入挖矿. 那么就需要通过竞拍获得资格. 竞拍使用的货币是 T$. 每次窗口出现的时候出价最高的 Seed 个矿工会获得机会加入挖矿. 没有获得机会的等待着继续竞拍下一个窗口期.
Any kind of hardware and software structure of the mining machine will be subject to price control when the quantity exceeds 1/3. That is to say, it is necessary to pay a higher seed purchase fee to obtain the seed.
Any kind of hardware and software structure of the mining machine will stop issuing new seeds when the quantity exceeds 1/2, and will not be able to recover until the ratio is lower than 1/2
This proportional control method contributes to the diversification of the software and hardware structure of the entire network, avoiding the occurrence of a loophole that can compromise more than 2/3 of the nodes.

Competition for Seed
When there are more than Seed miners who want to join mining, they need to be eligible for bidding. The currency used for bidding is T$. Each time the window appears, the seed miners with the highest bids get the opportunity to join the mining. Those who do not get the chance can wait for bidding to continue in the next window period.

如果没有足够的竞争者参与, 那么空余的 Seed 会作废, 不会顺延到下一个窗口期. 这种情况下很可能不需要花钱就可以加入挖矿.

拍卖获得的收益用于支付公共服务支出.

转让和购买 Seed
对于已经处于活跃状态下的矿工可以把自己的 Seed 转售给希望加入的新矿工. 价格由市场价格决定. 不过如果一个矿工已经由于自愿退出或者因为安全审计失败被开除从而失去活跃矿工资格的矿工会失去自己的 Seed, 当然也就不能销售了. 对于资源退出的矿工, 他的 Camellia 仍然存在, 可以销售,也需要缴税. 对于安全审计失败而被开除的矿工, Camellia 被没收为 0, 所以也没有可以卖的了.

由于 Camellia 可以在内部转让, 所以新矿工可以一并购买老矿工的 Camellia, 或者从其他矿工购买 Camellia 从而获得一个比较好的初始 Camellia. 当然, 也可以不购买, 自己慢慢积累.
If there are not enough competitors participating, the spare seed will be invalidated and will not be postponed to the next window. In this case, it is likely that you can join mining without spending money.

The proceeds from the auction are used to pay for public service expenditures.

Transfer and purchase Seed
Miners who are already active can resell their Seed to new miners who wish to join. The price is determined by the market price. However, if a miner has already voluntarily withdrawn or been expelled because of a failed safety audit, and thus loses the qualification of an active miner, the union loses its Seed, and of course it cannot be sold. For the miners whose resources have withdrawn, his Camellia still exists, can be sold, and also needs to pay taxes. For the miners who are expelled because of the failure of the security audit, Camellia is confiscated as 0.

Since Camellia can be transferred internally, new miners can buy Camellia from previous miners, or buy from others to get a better initial Camellia. Of course, miners also have the option to accumulate it themselves.

预售和融资
目前 TEA 项目已经完成了基础技术的研究和演示版本的开发. 准备进入正式产品和代币经济的开发. 为了完成这部分的工作需要进行快速融资.

目前考虑的融资手段是预售 Seed.

这些 Seed 的用户会在主网上线的时候开始预挖矿. 在预挖矿期间, 只有这些参与预售的矿机有权进入采矿. 这个阶段属于积累 Camellia 和 TEA token 的时期. 在这个期间交易的部分还在开发过程, 所以还不能交易.

等到预挖矿阶段结束, 对外公开的时间节点就是所有基础金融服务都完成的时间. 其他矿工可以通过竞拍 Seed 加入采矿行业. 已经挖出的 TEA 也可以在 Uniswap 等 DEX 进行正式交易. 对于已经在挖矿的 Presale 的矿工这时候也可以销售自己的 Seed 给这时候才知道参与的新矿工. 这些交易都是需要在这个节点之前就完成的基本金融服务功能.
Pre-sale and financing
As of now, the TEA project has completed research of the basic technology and development of the demo version. It is ready to enter the stage of development of the official product and token economy. In order to proceed forward to this next step, fast financing is required.

The financing method currently being considered is the pre-sale of Seed.

These Seed users will start pre-mining when the mainnet is online. During the pre-mining period, only these miners who are participating in the pre-sale have the right to enter the mining. This stage belongs to the period of accumulation of Camellia and TEA tokens.

When the pre-mining stage is over, the publicly available time node is the time when all basic financial services are completed. Other miners can join the mining industry by bidding Seed. TEA that has been mined can also be officially traded on DEX such as Uniswap. Presale miners who are mining can also sell their own Seed to new miners who only know about their participation at this time. These transactions are basic financial service functions that need to be completed before this node.

预售是 ICO 吗?
最终解释可能需要法律专家出面. 根据我的理解这个不是 ICO. 我们没有销售 token 给参与预售的人. 所有的 Token 都是参与预售的人自己跑矿机自己挖出来的. 而且我们的流通 Token 还是 Utility token, 本身也不是证券. Camellia 不能外部流通, 根本不能算是 token. 社区治理采用 DAO 模式, 并不存在一个类似基金会的机构掌控资金操纵币价的可能性.

预售的资金使用和去向
预售的资金用于立即开始一直到主网上线期间的产品开发费用. 如果有剩余部分. 会转入 DAO 管理用于支付未来的维护费用. 用 DAO 的投票机制管理. 这些资金不属于任何个人和基金会.
Is the pre-sale an ICO?
The final explanation may require legal experts to come forward. According to my understanding, this is not an ICO. We do not sell tokens to those who participate in the pre-sale. All the tokens were mined by people who ran their own mining machines. Our circulation Token is also a Utility token, so it is not a security in itself. Camellia cannot be circulated externally, and cannot be regarded as a token at all. Community governance adopts the DAO model, and there is no possibility that an institution similar to a foundation controls funds to manipulate the price of the currency.

Use and destination of pre-sale funds
The presale funds are used for product development costs from the immediate start to the mainnet launch period. If there are any remaining funds, they will be transferred to DAO management to pay for future maintenance costs. It is managed by DAO's voting mechanism; these funds do not belong to any individual..

预售的买家得到了什么
预售的购买者得到的是 Seed. 就是一个账号和私钥. 这个私钥需要自己保存好. 没有任何人知道你的私钥. 你的公钥就是矿工账号. 在预挖矿开始的时候, 拥有这些账号的矿工可以租用或者自建矿机开始挖矿. 这期间还没有完成交易所等金融服务应用, 所以只能挖矿, 不能买卖. 这个期间属于积累 Camellia 和 TEA token的时段. 因为这时候刚刚开始出矿, 还没有达到产量缩减, 也没有对外公开挖矿, 只有预售的矿工可以参与. 相对来说竞争小, 收益高, 但是 TEA token 还不能交易, 也没有市场价格.
What do pre-sale buyers get
Pre-sale buyers get Seed, an account and private key. This private key needs to be kept by the buyer themself. Their public key is the miner’s account. At the beginning of pre-mining, Miners with these accounts can rent or build their own mining machines to start. During this period, financial service applications such as exchanges have not been completed, so they can only mine, not buy or sell. This period belongs to the accumulation of Camellia and TEA tokens. At this time, the mining has just started, the output has not been reduced, and there is no public mining. Only pre-sale miners can participate. Relatively speaking, the competition is small and the profit is high, but the TEA token cannot be traded yet, so there is no market price.

预售的买家的未来可能收益
预售的买家率先获得 Camellia 和预挖的 T$. 从主网上线开始, 这些矿工就有权出售自己的 T$或者 Camellia 还有 Seed. 当然, 我们更鼓励长期持有. 因为在未来任何时候都可以在市场价格更满意的时候售出. 毕竟未来挖矿的难度肯定是越来越大, 产量越来越低. 最初获得的 Camellia 在未来的竞争中很容易处于优势地位.

平台开发者的权益
平台开发者已经投入的成本都作为 IOU 的方式在预售期间折算成为 Seed. 折算价格按照预售公布价格, 或者平均价格(假如存在多个批次价格不同的话). 在主网上线可以交易之前, 这些 Seed 也不能交易. 这一点和其他预售参与者是一样的.

平台开发者在获得 funding 之后的工作可以选择拿工资或者部分工资部分权益的方式. 作为部分权益就是相当于 Convertible Notes 的方式. 根据时间点拿到一个折扣价格, 在未来可以从 DAO 管理的开发资金中购买TEA token.
Possible future benefits of pre-sale buyers
Pre-sale buyers are the first to get Camellia and pre-mined T$. Starting from the mainnet launch, these miners have the right to sell their own T$ or Camellia and Seed. Of course, we encourage long-term holdings. Because in the future any holdings can be sold when the market price is more satisfactory. After all, the difficulty of mining in the future will definitely be greater and the output will be lower. The Camellia that was originally acquired will easily be in an advantageous position in future competition.

The rights of platform developers
The cost already invested by the platform developers is converted into Seed during the pre-sale as an IOU method. The converted price is based on the pre-sale published price, or the average price (if there are multiple batches with different prices). Before the main online line can be traded, these Seeds cannot be traded either, similar to other pre-sale participants.

After obtaining funding, platform developers can either choose to take a salary, or part-salary, part-equity. Part-equity is equivalent to Convertible Notes. Based on the point of time, a discounted price can be obtained from the development funds managed by DAO in the future Buy TEA tokens in China.

平台开发者自身也可以成为矿工. 和其他人待遇一样.

平台开发者如果退出项目, 那么已经支付的工资和 Seed 继续保持. 但是 Convertible Notes 就自行放弃了.

平台基础应用开发者的权益
基础的金融服务 DApp 定义为平台基础应用. 这里面包括但是不限于

钱包 Gluonwallet
Lock&Mint, Burn&Redeem 协议
内部的 DEX 交易所
这些应用自身可以收取服务费用, 但是在启动初期仍然按照平台开发的一部分算入平台开发成本中. 主网上线以后脱离开成为独立的应用, 自负盈亏, 参与其他 dApp 的竞争.

预售融资平台
未知

DAO 管理
采用和其他 Defi DAO 类似的方式进行社区治理. Camellia 是权益币. 是投票的权重币. 也是税收分红的依据.
Platform developers themselves can also become miners, but they will get the same treatment as everybody else.

If the developer quits the project, the salary and seeds already paid will continue to be maintained. But Convertible Notes will give up on its own.

The rights of platform basic application developers
Basic financial service DApp is defined as a platform basic application. This includes, but is not limited to:

Wallet Gluonwallet
Lock&Mint, Burn&Redeem agreement
Internal DEX exchange
The applications themselves can charge service fees, but they are still included in the platform development cost as part of the platform development at the initial stage. After the mainnet is launched, they will leave and become independent applications. They will be responsible for their own profits and losses as well as participate in the competition of other dApps.


DAO management
Community governance is carried out in similar ways to other Defi DAOs. Camellia is an equity currency; a voting weight currency. It is also the basis for tax dividends.


TEA 有两种代币.
- TEA(茶叶): TEA是代币的 Ticker,可以简写成为 `T$`, 这是一种可以自由流通的 Utility Token. 用于挖矿收益和服务费用. 它是与计算资源成本锚定的稳定币.
- Camellia(茶树):  代表矿工的信用水平和盈利能力. 作为总量恒定的内部权益代币. 它用于奖励长期诚信服务和违规惩罚. 这个数值是参与DAO 管理的投票权重也是锁仓获得税收收入的依据.

除了两种代币之外,还有一种并非是代币, 而是一种准入资格叫做 Seed. 用于控制新增矿工节点的名额. 每个新增矿工窗口期的名额是有限的. 如果有更多矿工想加入就需要通过竞拍来获得矿工资格. 有了种子才可以成为矿工来加入 TEA 挖矿. 矿工的通过执行系统分配的客户的计算任务获得服务费 TEA. 在 Ethereum 和其他区块链中通常这个概念成为 Gas. 矿工的级别使用 Camellia 来表示. Camellia 越高的矿工获得高价值计算任务的概率越高, 同时承担的社区责任和权力也就越高.这个体现在DAO 投票权重和税率. Camellia 因为是权益币, 拥有者通过锁仓即可参与税收分红. 因为 Camellia 代表盈利能力, 所以它也可以用于信用借贷的信用值. 

# 经济系统设计原则和目的

这个经济系统的设计原则是为了

- 通过建立信用体系, 营造一个可以under collateral 信用借贷的 Defi 的底层支持
- 通过不可修改的宪法和可以修改的社区治理来兼顾早期参与者和后期参与者的利益, 使得项目可以在早期投资者获益的同时始终保持新陈代谢从而长期发展
- 打造一个合法的 Utility token,规避法律风险
- 自动调节流动性, 让投机和投资得到控制和收益并存

# TEA Project 的基础技术知识极简版本

TEA Project 是一个底层技术项目. 涉及的技术细节比较深奥. 有兴趣的可以去看技术白皮书. 在这里我们列出以可以读懂本文的代币经济学设计为目的的基础知识. 

TEA 是一个介于传统区块链和 dApp 之间的可信计算层. 它扩充了现有区块链的两个信任根: 共识和密码学, 增加了一个硬件信任根. 这样使得 dApp 可以把昂贵和复杂的计算从区块链上挪到 TEA 这个 Layer2 上. 从而提高效率降低成本, 完成了以前无法进行或者无法承担的计算工作而并没有丧失安全性. 大致可以认为是云计算的去中心化改进或者区块链的硬件加速器.

TEA project 中也包含一个区块链的底层叫 Layer1, 不过这个 layer1 不是运行 dApp 的智能合约, 而是运行对 Layer2 的安全审计. dApp 的计算逻辑(比如俗称智能合约)是跑在 Layer2 的可信计算硬件, 也就是矿工的矿机上的. 通过可信硬件和区块链的共识让矿工无法作恶, 从而实现可信安全和隐私保护的去中心化计算. 

TEA project 除了底层基础链和二层协议之外, 还包括一些基础的金融应用, 比如信用局, 钱包,交易所, 抵押铸币等. 更多的应用需要社区开发者逐步参与和支持开发.

因为本文主要专注在代币经济学设计. 至于为什么 TEA 可以做到可信, 请参考更加详细的 TEA 技术白皮书中的阐述.

# TEA: T$ Utility Token 
## T$ 的产生和分配

TEA是代币的 Ticker,可以简写成为 `T$`, 这是一种 Utility Token.
它类似于 Ethereum 的 Gas. 它的作用是支付为客户或者系统内部公共服务消耗的成本. 这些成本包括计算存储和网络. 与常见的云计算计费类似.
在创始区块中不会包含任何创始 TEA 分配给团队或者早期投资人. 所有的 TEA 都是需要通过挖矿来得到.

### 获得 T$的方式

有以下方式可以获得 `T$`

- 矿工为用户提供可信计算服务获得用户支付的 gas和小费 tip
- 矿工为 TEA 内部的公共服务提供计算服务获得 layer1 增发的 TEA
- 任何人通过金融交易获得
- 任何 Camellia 持有人通过锁仓获得税收分红

### `T$`的增发, 总量和价格锚定
和 Camellia 不同, `T$` 没有总量恒定. 它的增发来源于公共服务产生的计算成本. 只要有用于全网公共服务的计算资源消耗, 就会有等量的 TEA 被增发出来被参与公共服务挖矿的矿工按照工作量比例分配. 当然需要区别开来的是当矿工为客户服务进行的计算消耗是客户支付 TEA 作为 Gas 而不是通过系统增发. 

随着网络规模扩大或者减小, 公共服务的资源消耗也会增加或者减少, 因此增发的 TEA 速率是随着网络规模上下浮动的. 在经济好转的时候, 更多矿工加入挖矿, 公共服务负担加重, TEA 增发速率加大. 反之当经济变差的时候增发速率会降低.

因为公共事务会一直存在, 所以长期来看 TEA 是持续增发的 Token.

由于计算的定价是客观的根据计算量来衡量(比如 CPU 指令, 占用时间, 网络流量或者存储大小和时间等),所以 TEA 是用计算成本锚定的稳定币. 

#### `T$`的价格波动和市场自动调节

虽然 TEA 是锚定计算成本的"稳定币", 但是当市场对计算任务的需求也会导致供需不平衡产生的价格波动. 比如说 TEA 上线初期, 也许上面的应用不发达, 没有太多的任务需要执行. 这时候矿工通过公共服务获得的 TEA 没有人来购买产生大量闲置卖单会产生价格下跌. 这时候对于原本通过其他中心化云计算的传统 App 也许发现这个价格低于租用传统云计算的价格, 从而购买 TEA 使用 TEA 的计算服务. 这种买单会促使价格上扬直至接近传统云计算的计算价格. 
而另一种情形会推高 TEA 的价格. 下文会提到基于安全性考虑, 我们会通过控制  Seed 来避免突然涌入的大量的来不及安全审查的矿工节点突破 BFT 的容错极限. 因为矿工的规模是缓慢增长的, 当TEA 上的 dApp 繁荣, 大量的计算任务出现排队处理的时候. 客户需要增加小费 Tip 来获得优先处理权, 这样对 TEA 的买单会增加, 价格会提高. 随着价格的提高更多矿工愿意购买 Seed 加入挖矿行列, 从而分散计算压力, 达到降低拥堵的作用. 随后 TEA 的价格就会回落. 通过这种市场机制进行自动调节, 让 TEA 的价格围绕着计算资源成本上下浮动. 

除了自然市场供需调节之外, 还有各种常规的金融操作可以帮助价格回归稳定, 比如抵押贷款, 信用贷款, 期货杠杆等等.

### 公共服务奖励和分配

公共服务是指维护系统可信而进行的节点安全审查, 出块, 代码维护和系统管理支出. 这些开销无法找到具体的支付对象, 获益者是全体社区. 所以定义为公共服务.
公共服务的开销通过每个区块凭空产生的新代币来根据为这些任务发生的计算消耗来进行分配. 在系统初期主要是出块服务和根据安全审查消耗的计算资源, 未来也许会增加各种 DAO 内部管理开销. 比如说如果某个节点在前一个时间周期被选中进行了 100 次对其他节点进行的安全审(RA)那么它根据计费系统记录的消耗资源占比获得这个阶段产生的公共服务奖励等比奖励. 这个过程俗称挖矿.

在TEA 可以进行市场交易或者提供计算服务之前, 挖矿是唯一获得 TEA 的方式.

## T$的交易, 和 ERC20 的 Lock&Mint , Burn&Redeem (LMBR) 协议
`T$`是在 TEA 网络内部的代币. 自身不是发行在 Ethereum 上的 ERC20 代币. 因此不能直接转移到 ERC20 兼容的钱包或者交易所进行交易. 但是 TEA 提供了 Lock&Mint and Burn&Redeem Protocol 可以通过锁定 TEA Network 上的代币获得 1:1 等值的 ERC20 Token t.eth.这个代币是标准 ERC20 代币, 可以在任何支持 ERC20 的 Defi 系统上进行各种金融交易. 如果交易完毕希望赎回原先锁定的`T$`, 则需要进行一次 Burn 操作, 然后原先的 TEA 代币会返回. 除了交易费之外没有其他金融损失. 
同样的做法适用于其他支持智能合约和多签的区块链, 比如 Polkadot 的 t.dot token

## 未来 TEA 上面建立的各种 Defi 业务

TEA 属于一个区块链基础服务平台. 未来随着生态的开展, 上面一定会产生各种 Defi 应用. 这些 Defi 应用可以直接调用 TEA 提供的可信计算服务, 从而完成传统的区块链无法达到的高吞吐和低 Gas 费. 这些 Defi 因为是构建在 TEA 之上的, 因此就不需要进行 ERC20 转换即可直接处理. 如果需要处理 ERC20 兼容的外部代币,可以使用同样的Lock&Mint, Burn&Redeem的协议进行.

## 矿工的成本

矿工的成本包括

- 矿机的购买或者租赁(第一期只有租赁 Amazon Nitro 虚拟机通过验证. 随后开发独立的低成本TEA 矿机用于购买)
- 电力和网络开销
- 支付安全审计的开销

因为 TEA 使用可信计算技术. 矿工需要自备或者租用矿机进行挖矿. 初步阶段, 只有 Amazon Nitro 可信虚拟机是认可的矿机. 未来我们会开发各种类型的矿机符合分散风险的要求. 这些不同构架的矿机包括

- 基于 TPM 的独立硬件矿机
- Google 基于 AMD Enclave 技术的虚拟矿机
- Microsoft 基于 Intel Enclave 技术的虚拟矿机

与 POW 类型的挖矿需要大量算力不同, TEA 基本上没有太多的电力消耗. 对硬件要求也不高. 属于绿色挖矿类型. 所以这方面的开销基本上可以忽略.

因为 TEA 要求对所有有资格进行计算的节点进行不间断的随机的不可逃避的安全审计. 只要机器在待命状态, 就有可能被审计. 被审计是需要支付审计方的费用. 如果不能支付或者审计失败则会被认为不再安全, 从而被剥夺参与挖矿的资格.并处罚金, 甚至严重的丢失全部 Camellia 后开除出网络.

在网络运行初期, 系统随着新区块增发的新 T$ 基本上可以全部 cover 这些审计费用, 因此矿工不需要单独支付. 但是随着节点数量增加和增发的 Token 减少, 这部分成本会逐步转移到矿工自身支付. 

如果市场变差, 矿工获得的任务收益还不足以支付它的日常开销的时候, 可以选择退出挖矿. 这样竞争会减少, 单个矿工的收益会增加, 从而实现自动调节市场平衡的作用. 矿工离场后原有的 Seed 会销毁. 原来的 Camellia 可以转让和卖掉. 

# Camellia

Camellia 在 TEA 网络内部是一个权益币. 它的存在有以下的目的

- 作为权益分配依据, 在锁定后即可参与税收收益的分红
- 作为投票权重参与 DAO 治理
- 作为长期诚实提供可信计算服务的奖励, 同时也是违规作弊的惩罚
- 作为超额借贷的信用抵押物

## Camellia 不是 Utility Token
Camellia 没有绝对数值意义. 也就是说一个 Camellia 不能 peg 到任何实体价值上. 这一点和 T$ peg 计算消耗成本不同.
Camellia 只有相对意义. 也就是你的账号上的 Camellia 占 Total Camellia 的比例.或者你的 Camellia 和你的竞争对手的 Camellia 的高低对比. 

## Camellia 增发, 产量随时间衰减和总量恒定

每个区块包含的 Camellia 的数量根据如下计算方式递减:从创始区块开始, 每个 Block 奖励 8 Camellia. 随后每 1M 个区块减少到之前的奖励的 80%. 根据每 6 秒钟出一个块计算. 大约 2 年的时候会经历10 次减产而奖励数量低于 1. 到此为止, 总共的 Camellia 的数量是37439440.37. 虽然增发还会继续, 但是当数字小到分配到矿工的账户上的数字小于 10 的-18 次方最小单位是就等于 0 了. 即停止增发了.


## Camellia 的 锁定状态,权益收益和税收

Camellia有两种状态, 一种是自由状态, 一种是锁定状态. 自由状态的 Camellia 不享有税收收益分红, 也不能被用于计算获得计算任务的权重和投票的权重. 

在自由状态下, Camellia 可以自由流通. 也就是说可以参与抵押, 销售.

在锁定状态下, 在承诺的时段内, Camellia 被锁定在合约内. 拥有者锁定后得到一个代币凭证. 在锁定期间的全网税收都会按照这个代币凭证的比例分配发放. 

关于税收下文会介绍

## Camellia 的获得和失去
分配每个区块的 Camellia 的原则是
- 多劳多得. 和矿工挖矿所得 TEA 线性相关
- Camellia 的占比取平方根后成为权重, 用以缓解贫富差距

计算方法为 
每个矿工自己的权重绝对值
````

weight_of_miner_i = tea_mined_by_miner_i_in_this_block * locked_camellia_of_miner_i.sqrt()

```

获得的 Camellia 数量

```
Camellia_income_for_miner_i = total_camellia_in_this_block * weigh_of_miner_i / total_weight_of_all_miners

````


从这个公式可以看出只有通过挖矿获得的 TEA 被用于计算权重, 通过交易获得的不能计算在内. 这样是鼓励矿工积极参与服务, 而且其结果得到共识承认. 而矿工锁定的 Camellia 需要平方根后按比例分配. 只有锁定的 Camellia 参与计算. 这样是鼓励锁仓来维护币价. 取平方根而不是直接等比分配的原因是为了减缓贫富差距.

所有用户除了挖矿获得分配Camellia之外还可以通过TEA内部交易获得. 因此即使不是矿工, 仍然可以拥有 Camellia只不过不能分配劳动奖励了. 非矿工拥有 Camellia 的主要动机是税收收益分红和金融套利. 

Camellia作为矿工诚实守信的奖励同样也用于不诚实守信的处罚. 当矿工存在作恶行为或者不当操作产生了不安全的计算环境, 被安全审计发现并共识认定不再安全可信, 则会被罚没甚至完全踢出网络.
处罚的这部分Camellia 被固定分配给检举者和参与评判的仲裁节点, 剩余部分销毁.

因为从整体上看 Camellia 的总量有限, 增量递减. 只有可能被罚没销毁而不会无限增加. Camellia 的数量直接影响盈利能力. 所以属于稀缺资产, 有增值空间

## Camellia 作为投票权重

只有锁定状态的 Camellia 可以用于计算投票权重. 

Camellia 的一个重要的作用就是在 DAO 治理中的话语权. DAO 投票的时候 Camellia 是作为权重产生的. Camellia 的另外一个作用是获得任务的机会加权. 


## Camellia的任务分配权重

只有锁定状态的 Camellia 可以被用于计算分配权重. 自由状态的不可以. 

在共识算法中计算节点分配到任务的几率和该节点的Camellia数值的平方根成正比. 设计成为非线性比例是弥补马太效应造成的贫富差距和阶级固化. 

对于任务中有对Camellia数值有强制要求的情况, 就需要在符合要求的范围内使用同样方式进行随机分配. 如果设定的条件过于严苛, 符合条件的节点很少, 会对用户的计算带来安全风险. 这一点我们需要提示给用户, 用户需要自行承担责任和风险.

## Camellia 的转手总额限制

为了避免女巫攻击, 也就是通过短时间聚集大量用户数和大量资金疯狂收购 Camellia 从而达到控制选举和共识机制的风险, 我们设置了全局 Camellia 转手限制. 如果前64 个区块总共发生了全网 Camellia 总额的 1/128的话, 这个区块讲不能打包任何涉及到 Camellia 转手的交易. 这些交易会顺延到下一个区块. 如果仍然超过, 就还是需要继续等待直到不再满足提交为止. 在交易不能达成期间 Camellia 仍然继续按照时间衰减, 所以交易的数额会在打包的时候重新计算或者取消. 

## 使用 Camellia 进行信用借贷

Camellia 可以认为是一种信用资产代表了对未来收入的预期. 高 Camellia 意味着高的未来 Gas 收入和更高的偿还能力. 因此 Camellia 可以用于超额借贷中的连带抵押物.

在 TEA 网络上的 Defi 应用可以把借款人的 Camellia 值作为是否发放贷款的参考依据. 根据借贷人的 Camellia 的数值可以制定合理的借款利率和不同的杠杆率. 
Camellia 不仅仅作为与其他抵押物一同作为信用参考值, 它自身也可以单独作为抵押物. 当借贷人无力偿贷的时候, Camellia 作为连带抵押物进行拍卖偿还贷款.
Camellia 一旦作为抵押物, 放贷人就成为它的 Lien holder. 尽管从账号上看仍然属于原来的主人的账号上, 还可以继续用于各项 Camellia 的权益. 



## Camellia 的破产拍卖交易

信用可以用于抵押物进行借贷. 那么在无法还贷的情况下就必须进行拍卖物抵押来偿还. Camellia 转手同样受到全网 Camellia 转手总额限制. 如果发生大量突发交易会自动拖延来避免女巫攻击来劫持投票和控制共识机制. 

## Camellia 的增值空间假设

早期的矿工由于竞争不激烈而且挖矿奖励高, 比较容易积累信用并相对于后来加入的新矿工具有权重上的优势, 所以更加容易获得任务积累财富. 但是随着活跃矿工增加以及产量降低, 计算任务分派概率和增发权重的时候都采用平方根的计算方式. 过于集中的 Camellia 并不会带来相应的高收益. 反而长久会造成社会分配区域平衡. 因此这时候是考虑卖出给新矿工获得投资收益. 这种方式有利于平衡新老矿工之间的利益, 促使项目可以长期发展.

## 税收和分红

税收来源于每一个区块所有账号通过计算任务(无论是公共服务还是有偿客户计算任务)获得的 TEA 收益. 按照一个可以通过DAO 调节的税率来收取. 初始数值设定为 0.3%.

这笔税收全部用于对锁定了 Camellia 的权益人按照锁定比例进行分发. 

# Seed 和计划生育

## 目的

通过控制新节点涌入的速度来避免来不及进行安全审核, 尤其是新平台的安全审计存在漏洞带来的 BFT 共识容错底线被突破的风险. 在客观上也造成了一定程度的稀缺性. 为金融投机提供了可能性

## Seed 的数值计算系数 Birth_rate

在任意一个给定时刻, 新区块里面允许增加的新矿工节点的数量叫做 Seed. 其计算方法是 

` Seed = math::round::ceil(total_Seed * (1 + birth_rate))`

在创始区块中有一个初始的 birth_rate, 未来可以通过一个算法来自动调节. 类似于 BTC 自动调节的难度系数. 不过 TEA 的出生率条件是根据任务拥塞程度来调节. 如果任务很少, 大量节点处于等待状态, 则说明市场不旺, 需要降低出生率避免恶性竞争. 如果任务很多, 甚至产生积压排队, 就需要提高出生率招募更多矿工来分摊任务和公共服务成本.

因为出块间隔比较短, 现在是 6s, 所以不是每个区块都允许有 Seed 的. 目前预计是每隔 128 个区块(约 12 分钟)Seed 个新矿工加入. 

## Seed 内部的多样性名额控制

为了防止女巫攻击, 以及过于集中的软件硬件架构造成不能及时发现的漏洞蔓延到超过 2/3 容错限制情况的发生. 在分配 Seed 的时候还需要额外遵循如下原则

- 任何一种软件硬件结构的矿机在超过 1/3 数量的时候开始受到价格控制. 也即是说需要支付更高的 Seed 购买费用来获得 Seed
- 任何一种软件硬件结构的矿机在超过 1/2 数量的时候就停止发放新的 Seed, 直到比例低于 1/2 才可以恢复

这种比例控制方式有助于全网软硬件结构的多样化. 避免发生一个漏洞可以攻陷超过 2/3 节点的情况

## 获得 Seed 的竞争

当有超过 Seed 数量的矿工希望加入挖矿. 那么就需要通过竞拍获得资格. 竞拍使用的货币是 T$. 每次窗口出现的时候出价最高的 Seed 个矿工会获得机会加入挖矿. 没有获得机会的等待着继续竞拍下一个窗口期.

如果没有足够的竞争者参与, 那么空余的 Seed 会作废, 不会顺延到下一个窗口期. 这种情况下很可能不需要花钱就可以加入挖矿.

拍卖获得的收益用于支付公共服务支出.

## 转让和购买 Seed
对于已经处于活跃状态下的矿工可以把自己的 Seed 转售给希望加入的新矿工. 价格由市场价格决定. 不过如果一个矿工已经由于自愿退出或者因为安全审计失败被开除从而失去活跃矿工资格的矿工会失去自己的 Seed, 当然也就不能销售了. 对于资源退出的矿工, 他的 Camellia 仍然存在, 可以销售,也需要缴税. 对于安全审计失败而被开除的矿工, Camellia  被没收为 0, 所以也没有可以卖的了.

由于 Camellia 可以在内部转让, 所以新矿工可以一并购买老矿工的 Camellia, 或者从其他矿工购买 Camellia 从而获得一个比较好的初始 Camellia. 当然, 也可以不购买, 自己慢慢积累.




# 预售和融资

目前 TEA 项目已经完成了基础技术的研究和演示版本的开发. 准备进入正式产品和代币经济的开发. 为了完成这部分的工作需要进行快速融资.

目前考虑的融资手段是预售 Seed. 

这些 Seed 的用户会在主网上线的时候开始预挖矿. 在预挖矿期间, 只有这些参与预售的矿机有权进入采矿. 这个阶段属于积累 Camellia 和 TEA token 的时期. 在这个期间交易的部分还在开发过程, 所以还不能交易.

等到预挖矿阶段结束, 对外公开的时间节点就是所有基础金融服务都完成的时间. 其他矿工可以通过竞拍 Seed 加入采矿行业. 已经挖出的 TEA 也可以在 Uniswap 等 DEX 进行正式交易. 对于已经在挖矿的 Presale 的矿工这时候也可以销售自己的 Seed 给这时候才知道参与的新矿工. 这些交易都是需要在这个节点之前就完成的基本金融服务功能.

## 预售是 ICO 吗?

最终解释可能需要法律专家出面. 根据我的理解这个不是 ICO. 我们没有销售 token 给参与预售的人. 所有的 Token 都是参与预售的人自己跑矿机自己挖出来的. 而且我们的流通 Token 还是 Utility token, 本身也不是证券. Camellia 是内部权益币, 不能直接外部流通, 根本不应算是 token. 社区治理采用 DAO 模式, 并不存在一个类似基金会的机构掌控资金操纵币价的可能性. 

## 预售的资金使用和去向

预售的资金用于立即开始一直到主网上线期间的产品开发费用. 如果有剩余部分. 会转入 DAO 管理用于支付未来的维护费用. 用 DAO 的投票机制管理. 这些资金不属于任何个人和基金会. 

## 预售的买家得到了什么

预售的购买者得到的是  Seed. 就是一个账号和私钥. 这个私钥需要自己保存好. 没有任何人知道你的私钥. 你的公钥就是矿工账号. 在预挖矿开始的时候, 拥有这些账号的矿工可以租用或者自建矿机开始挖矿. 这期间还没有完成交易所等金融服务应用, 所以只能挖矿, 不能买卖. 这个期间属于积累 Camellia 和 TEA token的时段. 因为这时候刚刚开始出矿, 还没有达到产量缩减, 也没有对外公开挖矿, 只有预售的矿工可以参与. 相对来说竞争小,  收益高, 但是 TEA token 还不能交易, 也没有市场价格.

## 预售的买家的未来可能收益

预售的买家率先获得 Camellia 和预挖的 T$. 从主网上线开始, 这些矿工就有权出售自己的 T$或者 Camellia 还有 Seed. 当然, 我们更鼓励长期持有. 因为在未来任何时候都可以在市场价格更满意的时候售出. 毕竟未来挖矿的难度肯定是越来越大, 产量越来越低. 最初获得的 Camellia 在未来的竞争中很容易处于优势地位.

# 平台开发者的权益

平台开发者已经投入的成本都作为 IOU 的方式在预售期间折算成为 Seed. 折算价格按照预售公布价格, 或者平均价格(假如存在多个批次价格不同的话). 在主网上线可以交易之前, 这些 Seed 也不能交易. 这一点和其他预售参与者是一样的.

平台开发者在获得 funding 之后的工作可以选择拿工资或者部分工资部分权益的方式. 作为部分权益就是相当于 Convertible Notes 的方式. 根据时间点拿到一个折扣价格, 在未来可以从 DAO 管理的开发资金中购买TEA token. 

平台开发者自身也可以成为矿工. 和其他人待遇一样.

平台开发者如果退出项目, 那么已经支付的工资和 Seed 继续保持. 但是 Convertible Notes 就自行放弃了.

# 平台基础应用开发者的权益

基础的金融服务 DApp 定义为平台基础应用. 这里面包括但是不限于

- 钱包 Gluonwallet
- Lock&Mint, Burn&Redeem 协议
- 内部的 DEX 交易所

这些应用自身可以收取服务费用, 但是在启动初期仍然按照平台开发的一部分算入平台开发成本中. 主网上线以后脱离开成为独立的应用, 自负盈亏, 参与其他 dApp 的竞争.


# 预售融资平台 DEX. IDO?

未知待定

# DAO 管理

采用和其他 Defi DAO 类似的方式进行社区治理. Camellia 是权益币. 是投票的权重币. 也是税收分红的依据.

