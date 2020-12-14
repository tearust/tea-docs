
# A basic Tensorflow image recognization apps running in a decentralized world

This is the easiest demo just like "Hello world". 

The background story of the demo is [here](./README.md)
![Story time](../res/demostory2.jpg)
Please make sure you read it before get hands dirty. It helps you understand what is happening and why.


# Do not get panic by "Not Secure."

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart1.png?raw=true)
When you click the easy start demo link, your browser may give you a warning on "Not Secure". 

Do not worry it is not a security threat. This is a normal *pure* dapp feed from IPFS. You can know from the URL in the picture (red box).

To learn more about why it is OK to be "not secure" and what is *pure* dapp mean, please go to "[under the hood](../FAQ/why_not_secure.md)".

# Prerequisites
  - Mac or Linux computer; We believe Windows computer should work too, but we haven't tested it yet. 
  - A Chrome or Firefox web browser which supports Polkadot plugin/extension ([How to install?](../FAQ/how_to_install_polkadot_extension.md))
  - [Create Polkadot account](../FAQ/how_to_create_a_new_account.md) using the extension
  - [Get some free test token](../FAQ/how_to_get_free_test_token_to_start.md) to make you rich enough to try our demo

# Start the dApp

From your browser installed with Polkadot extension, click this link [http://t-rust.com:8080/ipfs/QmUFLLDr6gXUctVAL28SuWKA3wtpAwQBYbePzLKKmdE3Yb/#/](http://t-rust.com:8080/ipfs/QmUFLLDr6gXUctVAL28SuWKA3wtpAwQBYbePzLKKmdE3Yb/#/). 

Because it is **pure** dApp, all resources need to be downloaded to your browser. The first time loading will take a few seconds. 

If you are behind the China Great Firewall, please use this Chinese local IPFS address instead: [http://81.70.96.136:8080/ipfs/QmbHfBZuLK41zf3nePiFstRTa81vAvpsf9HBQLycjw6VFb](http://81.70.96.136:8080/ipfs/QmbHfBZuLK41zf3nePiFstRTa81vAvpsf9HBQLycjw6VFb)

# Select an account

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart2.png?raw=true)

If you have not installed the Polkadot extension to your browser, you need to install now. 
If you have installed, there may be a pop-up box asking your permission to allow this web app access to the wallet. Grant permission since you will need to pay fake money using this extension during our demo. 

When you see the main page, the account lists here is actually the account in your extension wallet.

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart3.png?raw=true)
In my case, the account is "Kevin". All the payment in this demo will come from "Kevin" account. 


# Select a delegator node
Unless you deployed your TEA mining node (In the veteran session for advanced users), you will need to choose one of the bootstrap nodes. Bootstrap nodes are listed in the first table, named as "Alice", "Bob", "Charlie", and "Dave". They are the TEA nodes deployed by the TEA development team. Those nodes are for demo purposes only; choose "Bob" then click "Next".

# Pay deposit
After a few seconds, the delegator (Bob) responds to you as a "success". This means Bob has confirmed to be your delegator. You now can commit your task to Bob,
but before that, you need to make sure you have enough funds to pay for the transactions.


![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart4.png?raw=true)

In the red box, you can see 10/100/3309.9999. 
- Locked 10 units (Locked security deposit): You have 10 units currently used as a deposit to Bob. If you see any number rather than 0, that means you have an on-going task running. Bob needs to take 10 units from your deposit account as a "security deposit" to ensure workers will be paid when the task is completed. 
- Balance 100 units (Deposit Account): This is the current balance in your deposit account. When you submit a new task, the deposit will be taken from this account; not your main one.
- Layer1 Amount 3309.9999 (Main account): This is the balance in your account (In this demo case, it is my account "Kevin"). 

If you have no money in your main account, the Layer1 Amount shows 0. You cannot do anything. You can go to T-rust.com site [/Tool/Faucet](http://t-rust.com/tools/layer1_faucet) to get free tokens to continue. 

You also need to make sure your deposit balance (100 units in this picture) more than the cost of your task( in this demo it costs 10 units). Otherwise, when Bob is taking your security deposit, it will fail.

Transfer fund from the main account to deposit account by clicking "Deposit button". 

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart5.png?raw=true)

Input a number (since our demo task costs 10 units, deposit 100 units will let you try 10 times), then click OK.
When transfer completed, you can see the change in those two numbers.

# Password required for any payment from your extension
You probably have seen this already, when you transfer fund out of your main account, Polkadot extension will ask for your password.

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart6.png?raw=true)
This is the password you created when you generated your account in Polkadot extension. Keep it secure even you use fake money.

This dialogue box will be shown every time when transferring funds from your wallet. 

# Confirm the task

![notsecure](https://github.com/tearust/tea-docs/blob/main/res/easystart7.png?raw=true)

Now you can see the summary of the task you are going to submit.
## Deployed Code
This is the wasm code you are about to execute. 
Since you are running the "Easy-start" demo, you did not deploy code yourself. It is deployed by TEA project developers for you. However, you need to pay 3 units every time (pay_per_use in our screenshot). The price (3 units) is defined when developer deploy this code. You will learn more about the deployment in the mid-level demo. 
deployment_id is the ID of this wasm function. This ID is unique. It will change every time a new version of the code deployed to TEA network. Deployment_id is an essential concept. We will talk about it more in Under the Hood section. 

## Deploy Data
Similar to Deploying Code. This is the data (in our demo, a picture of a lion) you will run the wasm function as a parameter because this is the "easy start" demo. You do not need to deploy your own picture. The TEA project team has deployed a picture of a lion in the network. You need to pay for using it. There is no free lunch in the blockchain world. We will discuss the business model more in future sections.

The lion looks like this:
![lion](https://github.com/tearust/tea-docs/blob/main/res/lion.jpg?raw=true)
It looks very familiar, right? This is the lion Google used to demonstrate Tensorflow. If you do not like this picture, you can deploy your own data in our second demo. But let's complete this task first.

## Description
You do not need to change this JSON edit box unless you want to modify the revenue sharing model between Delegator and Executor. Please keep this in mind: if you pay too low to either Executor or Delegator, they may reject your work request because they work for money.

# Submit task and wait for the result
After review, the summary of the task, click "Run Errand Task". You will see
![run](https://github.com/tearust/tea-docs/blob/main/res/easystart8.png?raw=true)
It may take a few seconds to a few minutes depending on how many miners are working and how many tasks are waiting in the pool.
When it complete, you can see the lion and 67%. The Tensorflow think this picture is 67% likely to be a lion. No laughing, this is how AI see the world.

Suppose you did not see the result. Sorry, there must be something wrong. Let us know, and we will fix it. We are still at the "Thanks to God; it somehow works" moment".

