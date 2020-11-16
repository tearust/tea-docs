
# A basic Tensorflow image recognization apps running in a decentralized world

This is the easiest demo just like "Hello world". 



# Do not get panic by "Not Secure."

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart1.png?raw=true)
When you click the easy start demo link, your browser may give you a warning on "not secure". You can also see the "Not Secure" in your web browser like the picture above.

Do not worry it is not a security threat. This is a normal *pure* dapp feed from IPFS. You can know from the URL in the picture (red box).

To learn more about why it is OK to be "not secure" and what is *pure* dapp mean, please go to "![under the hood(/doc_list/%2FFAQ%2Fwhy-no-secure-website.md)".

# Prerequisites
  - Mac or Linux computer. Windows should work too, but we did not get a chance to test
  - A Chrome or Firefox web browser which supports Polkadot plugin/extension ([How to install?](../FAQ/how_to_install_polkadot_extension.md))

# Start the dApp
From your browser installed with Polkadot extension, click this link [http://t-rust.com:8080/ipfs/QmRfcEVcd4zb9osyUtCLLzEGVvpmKEYECgCDgzTuACQA2p/#/](http://t-rust.com:8080/ipfs/QmRfcEVcd4zb9osyUtCLLzEGVvpmKEYECgCDgzTuACQA2p/#/). 

Because it is **pure** dApp, all resources need to be downloaded to your browser. The first time loading will take a few seconds. 

If you are behind the China Great Firewall, please use this Chinese local IPFS address instead: [http://81.70.96.136:8080/ipfs/QmdxbhK5x993mJ58DVUJutXmSricz1ueHKFxPqfPrKUPMG](http://81.70.96.136:8080/ipfs/QmdxbhK5x993mJ58DVUJutXmSricz1ueHKFxPqfPrKUPMG)

# Select an account

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart2.png?raw=true)

If you have not installed the Polkadot extension to your browser, you may have to install now. 
If you have installed, it may pop up a box asking you to confirm you allow this web app access to the wallet. Accept it since you will need to pay the fake money using this extension during our demo.

When you see the main page, the account lists here is actually the account in your extension wallet.

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart3.png?raw=true)
In my case, the account is "Kevin". All the payment in this demo will come from "Kevin" account. 


# Select a delegator node
Unless you deployed your TEA mining node (In the veteran session for advanced users), you would better choose one of the bootstrap nodes. Bootstrap nodes are listed in the first table. They are named "Alice", "Bob", "Charlie", "Dave". They are the TEA nodes deployed by the TEA dev team. You can trust them at this time for test purpose. For example, you select "Bob" then click "next".

# Pay deposit
After a few seconds, the delegator (Bob) response to you as "success". That means Bob confirmed to be your delegator. You now can commit your task to Bob.
But before that, you need to make sure you have enough fund to pay for all the transactions.


![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart4.png?raw=true)

In the red box, you can see 10/100/3309.9999. 
- Locked 10 units (Locked security deposit): You have 10 units currently used as a deposit to Bob. If you see any number rather than 0, that means you have an on-going task running. Bob need to take 10 units from your deposit account as a "security deposit". Bob can make sure the workers will be paid when the task completed. 
- Balance 100 units (Deposit Account): This is the balance currently stay in your deposit account. When you submit a new task, the deposit will be taken from this account, not your main account
- Layer1 Amount 3309.9999 (Main account): This is the balance in your account (In this demo case, it is my account "Kevin"). 

If you have no money in your main account, the Layer1 Amount shows 0. You cannot do anything. You can go to T-rust.com site [/Tool/Faucet](http://t-rust.com/tools/layer1_faucet) to get free tokens to continue. 

You also need to make sure your deposit balance (100 units in this picture) more than the cost of your task( in this demo it costs 10 units). Otherwise, when Bob is taking your security deposit, it will fail.

Transfer fund from the main account to deposit account by clicking "Deposit button". 

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart5.png?raw=true)

Input a number (since our demo task is 10 units, deposit 100 units will let you try 10 times), then click OK.
When transfer completed, you can see the change in those two numbers.

# Password required for any payment from your extension
You probably have seen already, when you transfer fund out of your main account, Polkadot extension will ask you for a password.

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart6.png?raw=true)
This is the password you created when you generate your account in Polkadot extension. Keep it secure even you are using fake money.

This dialogue box will be shown every time when transfer fund from your wallet. 

# Confirm the task

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart7.png?raw=true)

Now you can see the summary of the task you are going to submit.
## Deployed Code
This is the wasm code you are about to execute. 
Since you are running the "Easy-start" demo, you did not deploy code yourself. It is deployed by TEA project developers for you. However, you need to pay 3 units every time (pay_per_use in our screenshot). The price (3 units) is defined when developer deploy this code. You will learn more about the deployment in the mid-level demo. 
deployment_id is the ID of this wasm function. This ID is unique. It will change every time a new version of the code deployed to TEA network. Deployment_id is an essential concept. We will talk about it more in Under the hood section

## Deploy Data
Similar to Deploying Code. This is the data (in our demo, a picture of a lion) you will run the wasm function as a parameter because this is the "easy start" demo. You do not need to deploy your picture. The TEA project team has deployed a picture of a lion in the network already. You need to pay to use it. What? Do I need to pay to use a picture? Yes, there is no free lunch in the blockchain world. We will discuss more the business model in future sections.

The lion looks like this:
![lion](https://github.com/tearust/tea-docs/blob/main/res/lion.jpg?raw=true)
It looks very familiar, right? This is the lion Google use to demo Tensorflow. If you do not like this picture, you can deploy your data in our second demo. But first, let's complete this task for now.

## Description
You do not need to change this JSON edit box unless you want to try to modify the revenue sharing model between Delegator and Executor. Make sure when you are modifying this, do not be cheap. If you pay too low to either Executor or Delegator, they may reject your request. They work for money!

# Submit task and wait for the result
After review, the summary of the task, click "Run Errand Task". You will see
![run](https://github.com/tearust/tea-docs/blob/main/res/easystart8.png?raw=true)
It may take a few seconds to a few minutes depends on how many miners are working and how many tasks are waiting in the pool.
When it complete, you can see the lion and 67%. The Tensorflow think this picture is 67% likely to be a lion. No laughing, this is how AI see the world.

Suppose you did not see the result. Sorry, there must be something wrong. Let us know, and we will fix it. We are still at the "Thanks to God; it somehow works" moment".

