# The background
![Story time](../res/demostory2.jpg)

The demo is a story about decentralized trusted computing between Alice, Bob, Charlie, and Dave. 
![Story time](../res/demostory3.jpg)
They play different roles in this story. One thing in common that they do not trust each other, but still need to cooperate to make such a business deal.

That's why they need T-rust as the decentralized trusted computing platform to carrier the computation.

![Story time](../res/demostory4.jpg)
Of course, they cannot make deal by themselves. Alice deploy her data (the picture) to T-rust, returning a Deployment_ID for her image.
Bob did the same to his code. Charlie setup a TEA module and join the T-rust network as a IPFS+TEA double miner.
Dave pay for the task and wait for the result


![Story time](../res/demostory5.jpg)
When the task complete, Dave receives the result (and a series of proot of trust). Alice, Bob and Charlie receive they payment. 


![Story time](../res/demostory6.jpg)
During the execution of this task, everything happened inside or between TEA nodes. The TEA nodes is an HSM protected by hardware and consensus. No one (including Charlie, the owner) has any information on what is going on, no to mention outside hackers.

Alice get paid by her picture without data leaking. None of Bob, Charlie and Dave has a copy of her picture.

Bob get paid for his Tensorflow algirhtm (model). None of Alice, Charlie and Dave has a copy of his code (or model).

Charlie know nothing about what happened, but he get paid for providing the hardware and services. He has zero knowledge about the task or any data.

Dave get the result as he expected. The proof of trust can be veriried so that he knowns the result is actually comming from the correct code and data he was requested.

This is how a typical decentralized trusted computing works!

# Start the demo
Before try any of these demos, please make sure you 
- read the [introduction](http://t-rust.com/#/demo) 
- installed required [extension](../FAQ/how_to_install_polkadot_extension.md)
- [created your own account](../FAQ/how_to_create_a_new_account.md)
- get some free tokens from our [faucet](../FAQ/how_to_get_free_test_token_to_start.md)

In this chapter, you will first try to run a simple "[easy start](Easy_start.md)" demo without deploying anything.

Then you can try to [deploy data first, then run adhoc data](Deploy_data_run_adhoc_code.md).

If that works, try a [reversed version, deploying code first, then run adhoc code](Deploy_code_run_adhoc_data.md).

At the last, you can run [create your own TEA node](Run_your_own_TEA_node.md) to be a miner.