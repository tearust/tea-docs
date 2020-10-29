# For what reason TEA's website and dApp shows "Not Secure" in the browser

Short answser is we do not need https, because we do not transfer any secrete in plain text between you and anyone else.

In most browser, if a webserver runs an https server, it is considered "secure". If a server runs an http server, it is considered "Not Secure". 

Https encrypted all the traffic between browser and server. Any sniffer in between cannot get the content. Only browser and server can decrypt the content.

But why doens't TEA need https?

Let's move to the long answer.

## Traditional cloud apps assume server can be trust, but we do not
In the traditional centralized cloud computing era, the basic assumption is that server can be trusted. So https is invented to prevent sniffer in the middle between client and server. No matter how secure https is, the content is available once it reaches the server.

In the decentralized TEA world, we do not have such an assumption. we have to assume that server is owned by a hacker. As long as the information reaches such a server, the hacker can read the secrete content on the server. 

This is the reason privacy breaching happens almost every day. I am not saying the service providers are bad guy. I am saying as long as hacker can break into the server, he can get whatever information on the server as long as not encrypted.

In TEA, we do not trust the server, but we trust a small hardware protected modules inside the server. We call it the TEA module. All the information outside of the TEA module is not secure. Secrete is decrypted only when it enter the TEA module, and encrypted again when leaving the TEA module. 

In this case, protecting the server turns to protecting a much smaller target - the TEA module. Smaller target has less attack surface, so it is much easier to get protected, and more secure.

## TEA dApps live on IPFS, not on server.
When you click the demo dApp, you actually connect to one of the IPFS servers all over the world. You do not care which IPFS node since they are all the same to end user. You ask the IPFS server to download the html js css code to you. Then run the code on your browser. The whole process has nothing to do with any web server. The dApp runs on your own browser.

## But where the Tensorflow algorithm runs?
Good question, we are not going to run the computation intensive Tensorflow algorithm on your browser. It actually runs on one of the TEA nodes all of the world. Again, you do not care and do not need to know which one actually runs your code. The blockchain consensus protects your data security and ensure the answer is correct. You can read more on the "Under the hood" section to get more detail.

## How did my secrete safely transfer to TEA module?
Because we do not trust server, all the secrete need to encrypted end to end. It is similar to https, just not between your browser and server, but between browser and the TEA module. Only TEA module can decrypt the content using a hardware protected key.

