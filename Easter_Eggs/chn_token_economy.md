中文版本 . TEA 代币经济设计
 
this document will be moved to website and docs when done
本文介绍了 TEA Project 的代币经济学设计. 关于 TEA Project 的基础技术介绍可以参考技术白皮书. 或者看下文中一个极简版本.
# Gist
TEA 有两种代币.
- TEA(茶叶): TEA是代币的 Ticker,可以简写成为 `T$`, 这是一种可以自由流通的 Utility Token. 用于挖矿收益和服务费用. 它是与计算资源成本锚定的稳定币.
- Camellia(茶树):  代表矿工的信用水平和盈利能力. 作为总量恒定的内部权益代币. 它用于奖励长期诚信服务和违规惩罚. 这个数值是参与DAO 管理的投票权重也是锁仓获得税收收入的依据.

除了两种代币之外,还有一种并非是代币, 而是一种准入资格叫做 Seed. 用于控制新增矿工节点的名额. 每个新增矿工窗口期的名额是有限的. 如果有更多矿工想加入就需要通过竞拍来获得矿工资格. 有了种子才可以成为矿工来加入 TEA 挖矿. 矿工的通过执行系统分配的客户的计算任务获得服务费 TEA. 在 Ethereum 和其他区块链中通常这个概念成为 Gas. 矿工的级别使用 Camellia 来表示. Camellia 越高的矿工获得高价值计算任务的概率越高, 同时承担的社区责任和权力也就越高.这个体现在DAO 投票权重和税率. Camellia 因为是权益币, 拥有者通过锁仓投资给矿工即可参与挖矿收益分红. 因为 Camellia 代表盈利能力, 所以它也可以用于信用借贷的信用值. 

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
- 任何 Camellia 持有人通过锁仓投资给信任的矿工获得收益分红

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

## 矿工的收益和成本

矿工的收益来自于为客户提供计算服务获得用户支付的计算费用和小费, 以及为公共服务提供的计算服务获得系统增发的$T 奖励.

分配这些服务除了自留利润之外, 还要为背后的支持者派发红利. 这些支持者是把自己的 Camellia 锁仓给矿工用来提供矿工的盈利能力的投资者. 

矿工的成本包括

- 矿机的购买或者租赁(第一期只有租赁 Amazon Nitro 虚拟机通过验证. 随后开发独立的低成本TEA 矿机用于购买)
- 电力和网络开销
- 支付安全审计的开销
- 资本成本, 就是分配给投资者的收益部分

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

- 作为权益分配依据, 在Staking锁定 给矿工后即可参与收益的分红
- 作为投票权重参与 DAO 治理
- 作为长期诚实提供可信计算服务的奖励, 同时也是违规作弊的惩罚
- 作为超额借贷的信用抵押物

## Camellia 不是 Utility Token
Camellia 没有绝对数值意义. 也就是说一个 Camellia 不能 peg 到任何实体价值上. 这一点和 T$ peg 计算消耗成本不同.
Camellia 只有相对意义. 也就是你的账号上的 Camellia 占 Total Camellia 的比例.或者你的 Camellia 和你的竞争对手的 Camellia 的高低对比. 

## Camellia 增发, 产量随时间衰减和总量恒定

每个区块包含的 Camellia 的数量根据如下计算方式递减:从创始区块开始, 每个 Block 奖励 8 Camellia. 随后每 1M 个区块减少到之前的奖励的 80%. 根据每 6 秒钟出一个块计算. 大约 2 年的时候会经历10 次减产而奖励数量低于 1. 到此为止, 总共的 Camellia 的数量是37439440.37. 虽然增发还会继续, 但是当数字小到分配到矿工的账户上的数字小于 10 的-18 次方最小单位是就等于 0 了. 即停止增发了.


## Camellia 的 锁定状态,权益收益

Camellia有两种状态, 一种是自由状态, 一种是锁定状态. 自由状态的 Camellia 并没有捆绑给某个矿机, 因此不能参与挖矿分红. 但是在自由状态下, Camellia 可以自由流通. 也就是说可以参与抵押, 销售. 

无论是自由状态还是锁定状态, Camellia 的投票权益都归属于 Camellia 的主人, 都可以参与投票. 

Camellia 的拥有者可以把自己的 Camellia 锁定给自己认可的矿工. 这个叫做 Staking. 锁定后的 Camellia 不能流通, 但是拥有者(不是接受投资的矿工)仍然享有投票权. 矿工的收益根据承诺的分配比例分配给锁定的 Staker 投资人作为红利. 矿工需要投资人Staking 的原因是增加 Camellia 提高盈利能力分散风险. 类似于 PoW 的矿池的概念. 

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

所有用户除了挖矿获得分配Camellia之外还可以通过TEA内部交易获得. 因此即使不是矿工, 仍然可以锁仓给认可的矿工获得挖矿收益, 或者通过金融交易套利. 

Camellia作为矿工诚实守信的奖励同样也用于不诚实守信的处罚. 当矿工存在作恶行为或者不当操作产生了不安全的计算环境, 被安全审计发现并共识认定不再安全可信, 则会被罚没甚至完全踢出网络.
处罚的这部分Camellia 被固定分配给检举者和参与评判的仲裁节点, 剩余部分销毁.

如果矿工受罚, 那么其身后的Staker 也会同比例失去 Camellia. 所以投资给矿工是有风险的. 所以只能投资给信誉好, 安全历史长的矿工. 

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

## 税收和用途管理

税收来源于每一个区块所有账号通过计算任务(无论是公共服务还是有偿客户计算任务)获得的 TEA 收益. 按照一个可以通过DAO 调节的税率来收取. 初始数值设定为 0.1%.

这笔税收的去向由 DAO 统一管理. 目前可以想得到的去向是 TEA Project 软件开发和维护的成本. 

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

采用和其他 Defi DAO 类似的方式进行社区治理. Camellia 是权益币. 是投票的权重币.
