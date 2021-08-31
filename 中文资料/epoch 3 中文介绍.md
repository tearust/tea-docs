# Epoch 3.0 vs Epoch 2.1 
### 金融业务方面的改进

## 任何人在任何时间都可以参加比赛
在 epoch 2.1, 只有在epoch开始之前注册的用户可以参加比赛。在epoch 3.0,任何人可以在任何时间参加比赛。

预先注册的唯一优势是注册用户将以固定价格获得 CML 优惠券（但不像 epoch 2.1 那样免费）。

## CML 优惠券不再免费
在比赛开始前注册的，仍然可以申请 CML 优惠券。但是用户在兑换优惠券时需要支付COFFEE。价格如下:

- 类型 A: 2000 COFFEE
- 类型 B: 1000 COFFEE
- 类型 C: 500 COFFEE


用户只能 **一次性** 兑换所有优惠券。例如，您不能在保持其他 CML 优惠券不变的情况下兑换一种 C 型种子。因此，当您填写注册表时，请确保您可以为每种类型的种子预先支付那么多的COFFEE费用。所有参赛者都可以以下面讨论的利率借用COFFEE。

## 所有转移交易都将被禁掉
您不能在不同账户之间转移资金或优惠券。这是为了防止作弊和避免使用多个帐户。

**所有资金转账交易都列在区块链上。任何违反禁止转移规则的人都将被取消资格并从奖励列表中删除。**

## 没有初始资金（但可以无限地使用 Genesis Loans of COFFEE）
![](../Blog_and_Vlog/Pasted%20image%2020210829121628.png)

您不会像在 epoch 2 挖矿比赛期间那样获得任何初始资金。但您现在可以不受限制地借用 COFFEE。当您需要资金时，您可以借用 COFFEE，然后按现行汇率将其转换为 TEA。但请注意，这是一种债务：COFFEE 每 100 个区块的复合利率为 0.2%（这个数字可能会发生变化。）如果您在这个时期积累资产的同时没有做好债务管理，您可能最终会负余额！

## 参赛者必须还清COFFEE债务，才有资格获得最终奖励

每个人都需要在 epoch 结束时还清所有的 COFFEE 债务。不这样做会导致被取消比赛奖励的资格。鉴于大多数人可能会在比赛临近结束时急于还清 COFFEE 债务，当许多人试图获得必要的 COFFEE 进行还债时，汇率可能会很高。 **考虑比其他人更早地还清 COFFEE 债务是明智的做法。**

## COFFEE 有信用利率和债务利率

在 epoch 2.0 中，没有 COFFEE 债务。如果您的帐户余额中有 COFFEE，您可以坐收复利。现在，由于您可以借 COFFEE，因此也会有债务利率。债务方与信贷方具有相同的复合利率。初始利率设置为每 100 个区块 0.2%。与 epoch 2 的 0.5% 初始速率相比，这要低得多。但由于这是一个复合利率，随着时间的推移，这个数字可能会导致账户余额不断攀升。借用 COFFEE 时，请注意您的贷款余额。

## DAO 可能会对 COFFEE 利率进行调整

DAO 可能会在比赛期间更改该值。我们会提前在群中通知任何利率变化。

## 请特别留意这是复利 

复利在开始时可能看起来只是一个小数字，但随着时间的推移，它可能会将您的负债余额变成一个可怕的数字。所以务必做好债务控制。

## Genesis TEA Loan 的可变利率由 AMM 曲线决定
在 epoch 3.0 中，您仍然可以使用冻结的 CML 种子作为 Gensis Loan 的抵押品。在 epoch 2 挖矿比赛中这个抵押贷款的利率为 0.1% 。现在，利率将根据 Genesis Loan 流动池中剩余的 TEA 决定。这是使用 AMM 曲线计算的。这意味着流动池中剩余的 TEA 越少，利率就越高。利率将是一个灵活的复利利率，每 100 个区块重新计算一次。因此，无论您贷款时的利率是多少，您支付的当前利率都是最近 100 块重新计算的利率。

![](../Blog_and_Vlog/Pasted%20image%2020210829123140.png)

## Genesis TEA Loans 可以全额还清或只是支付利息来延长贷款期限

在 epoch 2.1 中，您不能只支付利息来延长贷款期限。现在，只要您支付贷款到期时产生的利息，您就可以延长贷款期限。

![](../Blog_and_Vlog/Pasted%20image%2020210829123329.png)

当然您也可以选择在贷款到期时付清贷款。

您可以看到您的钱包中还有多少 Genesis TEA Loan 债务：

![](../Blog_and_Vlog/Pasted%20image%2020210829132950.png)

## 充值功能
在 epoch 2 中，一些参赛者因为剩余的 TEA 太低而无法进行任何交易而陷入困境。尽管最好避免在去加油站的路上耗尽汽油，这种情况有时仍然会发生。为了帮助用户摆脱这种困境（比如TEA 余额低于 0.0003），我们重新添加了**充值**按钮。您可以点击充值按钮获得0.1 TEA。它不会让您变得富有，但它至少会帮助您能把车开到加油站！

![](../Blog_and_Vlog/Pasted%20image%2020210829123656.png)


## 矿机不再免费。参赛者需要使用 COFFEE 购买矿机
在 epoch 3 中，开始挖矿时，您不但需要质押 1000 TEA  (或者质押一个种子 CML) , 你还需要使用 COFFEE 购买矿机。以下是在 epoch 3 中启动挖矿需要的条件：

- 解冻的种子 CML 种到矿机中。
- 1000 TEA 或者 1 个 CML (解冻或者未解冻的种子都可以) 作为矿机第一个质押位置的质押物.
- 需要支付矿机的 COFFEE 。

矿机价格取决于被种植的 CML 种子的类型。我们目前要求类型 A CML 支付 2000 COFFEE，类型 B CML 支付 1000 COFFEE，类型 C CML 支付 500 COFFEE。矿机不可重复使用。如果你从矿机上卸载 CML，那台矿机也不见了。

# Epoch 3 联合曲线投资

在 epoch 2 中，矿工有两种方式可以赚取 TEA：自己挖矿或质押另一个挖矿的 CML。

在 epoch 3 中，除了挖矿和质押之外，还有两种新的方式来获得 TEA 收入：

- 您可以通过 TApp 的联合曲线购买其代币从而成为该项目的投资者，这就类似风险投资家投资一个项目。
- 您可以使用您正在挖矿的 CML 托管 TApp 来赚取托管费。就像亚马逊向您收取云托管费一样，当您是提供云基础设施的矿工时，您将获得这笔费用。

 在 epoch 3 中，每个 TApp 将代表一个特定的 YouTube 视频。获胜视频（观看次数最多的视频）将获得 1500 美元的额外奖金，将分配给该TApp所有代币持有者。

## 投资 TApps 
在 epoch 3 中, 新增加了 TApps 页面.

![](../Blog_and_Vlog/Pasted%20image%2020210829133646.png)

在这个页面，您可以看见现有的 TApps，每个TApp后面的按钮用于投资或者托管该TApp。

**投资**意味着您将成为该 TApp 的股东，就像您购买公司的股票一样。
不同之处在于您是从称为 **联合曲线** 的智能合约中购买的。您向联合曲线支付 TEA 并获得特定的 TApp 代币。例如，在上面那个截屏中，如果您支付 TEA 购买它们，您将拥有 **DDF** 和 **TYB** 代币作为您的资产。代币的价格由 AMM 根据每个代币的联合曲线计算。一般来说，越早投资，价格越低。

![](../Blog_and_Vlog/Pasted%20image%2020210829135156.png) (此图中, n > 1, 但是我们假定 n = 1/2 and m = 1 和 0.7)

在 epoch 3 中, 我们使用基础的联合曲线 ![](../Blog_and_Vlog/Pasted%20image%2020210829134248.png)

**a** 为买入曲线为 1，卖出曲线为 0.7。积分 ![](../Blog_and_Vlog/Pasted%20image%2020210829134521.png)用于计算资金池和储备池的 TEA 金额。

如果联合曲线对你来说是一个新的 Defi 概念，请谷歌了解更多详情。简而言之，如果出售的代币越多（总供应量增加），则代币的价格和市值就越高。

![](../Blog_and_Vlog/Pasted%20image%2020210829134822.png)

## 卖出你的投资

与传统的订单薄市场不同，您在出售投资代币时不需要有买家。你实际上是把它卖给联合曲线。卖出价格基于预定义的规则，即**卖出曲线是买入曲线的 70%**。如果您购买代币并立即出售，您将损失 30%。 这部分资金将进到 TApps 所有者的资金池。

![](../Blog_and_Vlog/Pasted%20image%2020210829140043.png)

## Dividend (consumer usage) and expense(paying the hosting fee)

The income and expense of the TApp will go directly to and from the bonding curve as well. The TApp here is a simple DAO that is managed by code and not by the app developers. The bonding curve will automatically calculate how to distribute revenue to shareholders or take tokens from a wallet to pay for expenses.

![[Pasted image 20210829135046.png]]

When a consumer pays to use this YTB TApp, the funds will be distributed based on the bonding curve's predefined logic. This also hold true for the expenses, such as paying for hosting fees.

The bonding curve is constantly changing. Every consume and expense event will make the price change a little. This is how a typical AMM (Automatic Market Maker) application works to attract venture capital.

![[Pasted image 20210829135617.png]]

Once you've invested in any TApps, you can see them in your Assets page under the **My investment in TApps** tab:

![[Pasted image 20210829134905.png]]

## What if I have no idea about bonding curves and fancy equations?
It's not important that you understand all the nuances of the bonding curve in order to use it effectively just as you don't need to know how an engine works to drive a car. Very few people in the world totally understand how Wall Street works but they still use their financial services every day. Of course, those who understand the important aspects of the financial system are in a better position to make more money. 

If you don't yet understand how the bonding curve works to set prices, try to buy or sell a TApp's token and notice how the price changes. Sooner or later you'll get the gist of how the bonding curve price correlates with supply. Bonding curves are becoming an increasingly important part of more and more crypto projects, so learning about them now will put you ahead of those Wall Street people. 

# Epoch 3: hosting TApps = hosting income
TApps need to be hosted in mining machines to run. This is exactly what the TEA Project is designed for - to make a decentralized cloud computing platform. 

If your mining machine starts without hosting any TApp, it just makes the basic RA (Remote Attestation FaaS public service fee). That amout is very little, not even enough to cover the COFFEE interest you paid for the loan amount to buy your machine. So to prevent financial insolvency, you have to find a more profitable usage of your mining machine, which is to host TApps and earn a hosting income. That is the better way to utilize your mining machine.

## Host / unhost TApp
![[Pasted image 20210829140839.png]]

In the TApp list, you can host or unhost TApps for your mining CML. There are few important rules you will need to know.

### Performance requirement and remaining performance

Your CML has to have enough **remaining performance** to cover the cost of the TApp's **Host performance requirement**.  Because your CML has limited performance, the TApps it can possibly host are also limited. With this limitation, you should be smart enough to choose the TApps that make the most out of your CML's performance.

### Current /Max hosts

For most TApps, as long as the hosting CML reaches a minimum threshold, the application performance will be good enough. More hosting CMLs for the TApp won't increase performance past a point and sometimes might even cause the performance to degrade. So every TApp has to have an upper limit called **Max hosts**. 

Another consideration is the cost of hosting. The more hosts a TApp has, the more the TApp will need to pay for its hosting fee. So if there's a popular and profitable TApp in the list, you'll need to rush to host it before it reaches the max hosts number.

In epoch 3, we simply set **Max hosts** to a fixed value. In real life, these numbers are constantly changing due to the scale changes as required by the TApp.

## YTB TApp simulator
The TApps for epoch 3 will be simulated TApps each based on a YouTube video that covers some aspect of the TEA Project. We have a non-playing character (NPC) called **sudo** who will create 3 video TApps, and pay TEA as a consume action every day based on the view numbers on YouTube. The sudo account will check YouTube view numbers at a moment in time each day. The one who has the largest increase will win the TEA for that day.

- The sudo account notes who has the largest gain in views compared to 24 hours ago and notes down the increased view count (let's call it **delta**) of the winner for that day.
- The sudo account pays one TEA for each increased view of the winner (**delta** TEA in total) using the "consume" function every day. For example, let's say video A has the most views in the past 24 hours. It was at 100 views yesterday but now is at 180 views today. Sudo will consume 80 TEA into video A's TApp bonding curve.

## Tips and tricks for new epoch 3
Many of you have probably gained many tips and tricks from epoch 2. Most of them are still valid for epoch 3, but some of strategies will need changing. You can learn about and share your best contest strategies over at our [mining contest strategy discussion](https://github.com/tearust/teaproject/discussions/31).

## Hosting and investments makes much more than dumb mining

Dumb mining means you start a mining CML but do not host any TApps. In this case, the CML will only run the public services like RA which makes very little money. To be more competitive, try hosting TApps to earn the hosting fee.

As long as you make some TEA from mining or simply from incurring COFFEE debt, use your TEA to invest to the bonding curve of TApps. If you invest in the correct TApp, it makes much more than the compound interest. Of course, if you don't choose wisely, that will affect your standing on the leader board. Your total asset valuation is calculated based on how many TApp tokens you own multiplied by the current token price. Because the market cap of your bonding curve tokens is part of how your assets are evaluated onn the leader board, it's very important to choose your YTB TApp wisely.

## YTB TApps contest
Contestants can choose to invest in a YouTube videos TApp and then use their social influence to increse the value of their YTB Tapps investment. They can use curation marketing and their social media influence to pump up the views by sharing the YouTube link and spreading its popularity on social media.
