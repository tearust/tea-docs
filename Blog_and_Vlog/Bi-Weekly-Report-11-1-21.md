### TEA Project Bi-Weekly Report – November 1, 2021

![](https://cdn-images-1.medium.com/max/1600/1*Y5m2S8POSFHovkNdAk8Enw.png)

### Epoch 5 Mining Contest Progress

The epoch 5 mining contest will finish on November 6th. The biggest change from epoch 4 is that contestants need a cloud virtual machine to mine. This has resulted in fewer overall mining machines during the contest owing to increase cost paid out by the miner and increased technical ability required to run a miner.

-   Miners are responsible for keeping their mining machines running. Any miners that go offline without first unhosting have their deposits slashed. This incentivizes miners to pick good cloud providers while keeping engaged with the contest less they lose their mining deposits.
-   Those without the technical skill, patience, or initial funds to run a mining machine can still procure CML seeds and stake them into other contestants’ machines. This allowed all contestants to share in the mining rewards as long as they held Camellia.

There has been strong demand among miners with an average of around 40 mining machines during the epoch 5 contest. Some mining machines have had over 20 users staking to them, which shows strong participation among those not able to run a mining machine themselves.

### Moving Towards Epoch 6: A New TApp + New Mining Opportunities

-   Internal testing is nearing completion for our next major TApp, a messaging app named **TEA Party**. Users have requested the ability to broadcast messages to other users (e.g. if they are looking to buy or sell CML seeds). TEA Party allows them to pay **T** to send these messages while remaining in the decentralized and secure TEA network.
-   Epoch 6 will allow **type C CML** to mine without needing to run a cloud server. They will have simple public service tasks like making sure B CML machines remain online. Because they won’t be hosting TApps, they don’t need to be continuously online and home computers should suffice for C CML mining.

### Looking Ahead: Moving from DigitalOcean to AWS Nitro

Our most used provider for epoch 5 was DigitalOcean with many miners opting to mine with their droplets. Although fine for simulated mining, the TEA Project’s mining machines will eventually need hardware security modules to become a trustable part of the network like those found in [AWS Nitro](https://aws.amazon.com/ec2/nitro/) cloud servers. Nitro cloud servers are able to create secure enclaves using TPM-like device called the Nitro Security Module. 

We’re happy to report that the team has the TEA Project running on AWS Nitro cloud servers. The only issue of running these instances is the cost as AWS Nitro servers are much more expensive than traditional EC2 instances. In order to defray costs and to help support our development efforts, the TEA Project has applied for the [AWS Activate grant](https://aws.amazon.com/activate/). This will provide us with AWS computing resources that can be used by both the dev team and our testers. 

![](https://cdn-images-1.medium.com/max/1600/1*sjcBeKZX_7NUj3o8p4DW8g.png)

### One More Thing: DOT Ecosystem Parachains

Parachain slots for both Kusama (started in June, 2021) and Polkadot (November 11, 2021) are now being [auctioned off](https://parachains.info/auctions). Towards the goal of competing for either a Polkadot or Kusama parachain auction slot, the dev team has started looking into integrating [Cumulus](https://github.com/paritytech/cumulus) into their layer-1 consensus. Cumulus is a prerequisite for inter-chain communications on both the Polkadot and Kusama networks. You can track the progress on these and other developments by subscribing to our Medium blog as well as joining our Twitter.

[![](https://cdn-images-1.medium.com/max/1600/1*yEPGm8CPEAZ7KW7pXtxslw.png)](https://twitter.com/intent/follow?original_referer=https%3A%2F%2Fpublish.twitter.com%2F%3FbuttonType%3DFollowButton%26query%3Dhttps%253A%252F%252Ftwitter.com%252Fchris_herd%26widget%3DButton&ref_src=twsrc%5Etfw&region=follow_link&screen_name=teaprojectorg&tw_p=followbutton)