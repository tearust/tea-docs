# Epoch 3.0 vs Epoch 2.1 
### Changes in Financial Services

## Anyone can join at any time
In epoch 2.1, only those who registered before the epoch started could join the contest. Now in epoch 3.0, anyone can join the contest at any time. 

The only advantage of registering upfront is that the registered users will be offered CML coupons at a fixed price (but not free as in epoch 2.1.) 

## CML coupons are no longer free
Those registering before the start of the contest can still apply for CML coupons. But the user needs to pay COFFEE when redeeming their coupons. The price will be as follows:

- Type A: 2000 COFFEE
- Type B: 1000 COFFEE
- Type C: 500 COFFEE

Users can only redeem all of their coupons **at once**. For example, you cannot redeem one type C seed while keeping your other CML coupons untouched. So when you fill in the registration form, make sure you're OK to pay that much COFFEE upfront for each type of seed. COFFEE can be borrowed by all contestants at an interest rate to be discussed below.

## All transfers are disabled
You cannot transfer funds or coupons between different accounts. This is to prevent cheating and to disincentivize the use of multiple accounts.

**All fund transfer transactions are listed on the blockchain. Anyone breaking the no-transfer rule will be disqualified and removed from the rewards list.**

## No initial funding (but unlimited Genesis Loans of COFFEE)
![[Pasted image 20210829121628.png]]

You won't have any initial funding as you did during the epoch 2 mining contest. But you can now borrow COFFEE with no limitations. Whenever you need funds, you can borrow COFFEE, and then convert it to TEA at the prevailing exchange rate. But take note that this is a debt: COFFEE has a compound interest rate of 0.2% per 100 blocks (this number is subject to change.) If you don't manage your debt well while accumulating assets during this epoch, you might end up with a negative balance!

## COFFEE debt must be paid off for contestants to be qualified for the final rewards

Everyone needs to pay off all of their COFFEE debt at the end of the epoch. Failure to do so results in disqualification for any contest rewards. Given that most people may rush to pay off COFFEE close to contest end, the exchange rate may be high at that point when many are attempting to get the necessary COFFEE for repayment. **It would be wise to consider paying off your COFFEE debt earlier than others.**

## COFFEE has both a credit and debt interest rate
In epoch 2.0, there was no COFFEE debt. If you had COFFEE in your account balance, you could let it sit and earn compound interest. Now, since you can borrow COFFEE, there will be a debt interest rate as well. The debt side has the same compound interest rate as the credit side. The initial interest rate is set to 0.2% per 100 blocks. Compared to the 0.5% initial rate of epoch 2, this is much lower. But since it's a compound rate, the number could result in a climbing account balance over time for the amount borrowed. Please keep a cautious eye on your loan balance when borrowing COFFEE.

## COFFEE interest rate may be changed by the DAO
The interest rate is not a constant number. The DAO may change the value during the contest. We plan to give advance notice of any interest rate changes in our telegram group. 

## Be aware of compound interest
The compound interest rate may look like just a tiny number at the beginning, but it may turn your balance into a scary number over time. Make sure you always keep your debt under control. 

## The Genesis TEA Loan has a variable interest rate given by the AMM curve
In epoch 3.0, you can still use your frozen CML seeds as collateral for a Genesis Loan. The interest rate for our first mining contest in epoch 2 was 0.1 % flat. Now, the rate will change based on the remaining TEA in the liquidation pool of the Genesis Loan. This rate is calculated using the AMM curve: the less TEA there is remaining in the liquidation pool, the higher the interest rate. The interest rate will be a flexible compound interest rate that is recalculated every 100 blocks. So no matter what the rate it was when you took out the loan, the current interest rate you pay is whatever the rate is for the most recent 100-block recalculation. 

![[Pasted image 20210829123140.png]]

## Genesis TEA Loans can be paid off in full or just the interest to extend the loan
In epoch 2.1, you couldn't pay just the interest due to extend your loan. Now you can extend a loan by paying the interest accrued by the end of the loan due date. 

![[Pasted image 20210829123329.png]]

You still have the option to pay off the loan entirely. 

You can see how much Genesis TEA Loan debt you have outstanding in your wallet:

![[Pasted image 20210829132950.png]]

## Top up is back
During epoch 2, several contestants fell into trouble when their remaining TEA was too low to make any transactions. Although it's always best to avoid running out of gas on the way to the gas station, sometimes it still happens. To help those who've fallen below the approximately .0003 TEA balance necessary to make transactions, we've added back the **top up** button. You can click the top up button to get 0.1 TEA. It won't make you rich, but it'll at least help you drive to the gas station!

![[Pasted image 20210829123656.png]]

## Mining machines are no longer free. Contestants will use COFFEE to buy one
Youll now not only need to pay the 1000 TEA stake (or 1 staked CML) to start mining, epoch 3 will also require paying COFFEE to buy a mining machine. From now on, this is what's needed to start a mining machine during epoch 3:
- a defrosted CML seed to plant into the mining machine.
- 1000 TEA or 1 CML (defrosted or not, doesn't matter) for the initial staking slot.
- an amount in COFFEE to pay for the mining machine itself.

The mining machine price in COFFEE depends on the type of CML seed that's being planted. We currently require any type A CML to pay 2000 COFFEE, any type B CML to pay 1000 COFFEE, and any type C CML to pay 500 COFFEE. The mining machine is not reusable. If you unplant a CML from a mining machine, that mining machine is also gone.

# Epoch 3 Bonding Curve Investment
In epoch 2, there were two ways for miners to make TEA mining income: mining yourself or staking into another mining CML. 

In epoch 3, there are two new ways to make TEA income besides only mining and staking. 
- You can be an investor of a TApp by buying into its Bonding Curve. You invest in a project just like venture capitalists do.
- You can host a TApp using your mining CML to earn a hosting fee. Just like Amazon charges you a cloud hosting fee, you're paid this fee when you are a miner providing the cloud infrastructure. 

For epoch 3, each TApp will represent a particular YouTube video. The winning video (the one with the most views) will receive a separate prize of $1500 to be distributed to its token holders.

## Invest in TApps
In epoch 3, there's a new top-level TApps page.

![[Pasted image 20210829133646.png]]

This page shows the existing TApps and buttons allowing you to either invest or host any particular TApps.

To **invest** means you're a shareholder of this TApp, just like when you buy a company's stock. 
The difference is that you're buying from a smart contract called a **bonding curve**. You pay TEA to the bonding curve and receive a particular TApp token in return. For example, in the screenshot above, you'll have **DDF** and **TYB** tokens as your assets if you pay TEA to buy them. The AMM calculates the price of the token based on each token's bonding curve. Generally speaking, the earlier you invest, the lower the price.

![[Pasted image 20210829135156.png]] (in this image, n > 1, but we set n = 1/2 and m = 1 and 0.7)

In epoch 3, we use the basic bonding curve of ![[Pasted image 20210829134248.png]]
The **a** is 1 for the buy curve, 0.7 for the sell curve. The integral ![[Pasted image 20210829134521.png]] is used to calculate the TEA amount for the funding and reserve pools.

If the bonding curve is a new Defi concept to you, please google for more details. Simply put, if more tokens are sold (total supply increases), the higher the price of the token and the market cap.

![[Pasted image 20210829134822.png]]

## Sell your investment

Unlike traditional order book marketplaces, you don't need a buyer when you sell your investment token. You're actually selling it to the bonding curve. The sell price is based on the predefined the rule that **the sell curve is 70% of the buy curve**. If you buy a token and sell it immediately, you'll lose 30%. The 30% goes to the TApps owners' funding pool. 

![[Pasted image 20210829140043.png]]

## Dividend (consumer usage) and expense(paying the hosting fee)

The income and expense of the TApp will go directly to and from the bonding curve as well. The TApp here is a simple DAO that is managed by code and not by the app developers. The bonding curve will automatically calculate how to distribute revenue to shareholders or take tokens from a wallet to pay expenses.

![[Pasted image 20210829135046.png]]

When a consumer pays to use this YTB TApp, the funds will be distributed based on the bonding curve's predefined logic. This also holds for the expenses, such as paying for hosting fees.

The bonding curve is constantly changing. Every consume and expense event will cause the price to fluctuate. This is how a typical AMM (Automatic Market Maker) application works to attract venture capital.

![[Pasted image 20210829135617.png]]

Once you've invested in any TApps, you can see them on your Assets page under the **My investment in TApps** tab:

![[Pasted image 20210829134905.png]]

## What if I have no idea about bonding curves and fancy equations?
You don't have to understand all the nuances of the bonding curve in order to use it effectively, just as you don't need to know how an engine works to drive a car. Very few people understand how Wall Street works but they still use their financial services every day. Of course, those who understand the important aspects of the financial system are in a better position to make more money. 

If you don't yet understand how the bonding curve works to set prices, try to buy or sell a TApp's token and notice how the price changes. Sooner or later, you'll get the gist of how the bonding curve price correlates with supply. Bonding curves are becoming an increasingly important part of more and more crypto projects, so learning about them now will put you ahead of those Wall Street people. 

# Epoch 3: hosting TApps = hosting income
TApps need to be hosted in mining machines to run. This is exactly what the TEA Project is designed for - to make a decentralized cloud computing platform. 

If your mining machine starts without hosting any TApp, it just makes the basic RA (Remote Attestation FaaS public service fee). That amount is very little, not even enough to cover the COFFEE interest you paid for the loan amount to buy your machine. So to prevent financial insolvency, you have to find a more profitable usage of your mining machine, which is to host TApps and earn a hosting income. That is the better way to utilize your mining machine.

## Host / unhost TApp
![[Pasted image 20210829140839.png]]

In the TApp list, you can host or unhost TApps for your mining CML. There are few important rules you'll need to know.

### Performance requirement and remaining performance

Your CML has to have enough **remaining performance** to cover the cost of the TApp's **Host performance requirement**.  Because your CML has limited performance, the TApps it can host are also limited. With this limitation, you should be smart enough to choose the TApps that make the most out of your CML's performance.

### Current /Max hosts

For most TApps, as long as the hosting CML reaches a minimum threshold, the application performance will be good enough. Increasing the number of hosting CMLs for the TApp won't improve performance past a point and sometimes might even cause the TApp to degrade. So every TApp has to have an upper limit called **Max hosts**. 

Another consideration is the cost of hosting. The more hosts a TApp has, the more the TApp will need to pay for its hosting fee. So if there's a popular and profitable TApp in the list, you'll need to rush to host it before it reaches the **Max hosts** number.

In epoch 3, we simply set **Max hosts** to a fixed value. In real life, these numbers are constantly changing due to the scale changes as required by the TApp.

## YTB TApp simulator
The TApps for epoch 3 will be simulated TApps each based on a YouTube video that covers some aspect of the TEA Project. We have a non-playing character (NPC) called **sudo** who will create 3 video TApps, and pay TEA as a consume action every day based on the view numbers on YouTube. The sudo account will check YouTube view numbers at a specific time every day. The video who has the largest increase in views will win the TEA for that day.

- The sudo account figures who has the largest gain in views compared to 24 hours ago and records the increased view count (let's call it **delta**) for that video.
- The sudo account pays one TEA for each increased view of the day's winning video (**delta** TEA in total) using the "consume" function every day. For example, let's say video A has the most views in the past 24 hours. It was at 100 views yesterday but now is at 180 views today. Sudo will then consume 80 TEA into video A's TApp bonding curve.

## Hosting and investments make much more than dumb mining

Dumb mining means you start a mining CML but do not host any TApps. In this case, the CML will only run public services like RA, making very little money. To be more competitive, try hosting TApps to earn the hosting fee.

As long as you make some TEA from mining or simply from incurring COFFEE debt, use your TEA to invest in the bonding curve of TApps. If you invest in the correct TApp, it will make much more than COFFEE's compound interest. Of course, if you don't choose wisely, that will affect your standing on the leader board. Your total asset value is calculated based on how many TApp tokens you own multiplied by the current token price. Because the market cap of your bonding curve tokens is part of how your assets are evaluated on the leader board, it's very important to choose your YTB TApp wisely.

## Tips and tricks for new epoch 3
Many of you have probably gained many tips and tricks from epoch 2. Most of them are still valid for epoch 3, but some of the strategies will need changing. 

For example, the YTB TApps are now part of the contest and the YouTube video's tokens that you invest in are a core part of your assets. Contestants can use a content curation strategy to increase the value of the YouTube video's TApp they've invested in. They can do this by using their social media influence to pump up the views by sharing the YouTube link and spreading its popularity on social media. This is how someone can use their social influence to increase the value of their YTB Tapp investment.

You can learn about the best contest strategies and share your own over at our [mining contest strategy discussion](https://github.com/tearust/teaproject/discussions/31).