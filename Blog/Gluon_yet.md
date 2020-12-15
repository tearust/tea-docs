# Gluon (Distributed hardware wallet)— Yet another crypto wallet? Why? What’s new?

In case you have not read my previous blog [“Can trusted-computing protect your digital assets”](../Can_trusted_computing_protect_your_digital_assets.md), please read it first. So you will know what Gluon Wallet is. At least you will know Gluno is NOT a wallet (although it is called Gluon Wallet), it is actually a Trust-as-a-Service (TaaS) application focus on crypto keys.

![](../res/blog/0_q-o2ME7lRtdgCqkC.png)

## You say “I need a hardware wallet”, I heard “I need some way to protect my private key”

That’s true, you do not need whatever kind of wallet as long as you have a better way to protect your private key.

As I mentioned in my previous blog, (I bet you have read already) even a hardware wallet has caveats that put your digital assets at risk. What Gluon provides you is actually a Trust-as-a-Service. The trust comes from thousands of hardware wallets although you do not own them. You do not need to trust the owners of those hardware wallets, because they have no access to your secret, even you do not?

## What? I do not even have access to the private key as an owner?

Sorry but you do not. If you really want, you can have a partial key as additional protection (although we do not think it is necessary). Having a full private key in your pocket is actually a bad idea. If you think you have stronger protection than those thousands of hardware wallets, then you probably do not realize what protection means. In my mind, as long as there is a decrypted secret ever expose to any computing device which potentially is able to connect to a network, the secret is no longer secure, unless the device is particularly designed and hardware protected. So I think it would be more secure to generate and store your private key in Gluon all its lifetime. It should never leave the protected environment even when it is used to sign your transaction.

## Gluon password is your only master password to the Blockchain World

Since all your private keys to other blockchains are generated and stored inside Gluon, the only thing you need to remember is the Gluon password. It is actually a standard Substrate blockchain private key. You can use a browser extension or whatever software or hardware wallet.

![](../res/blog/WX20201215-105514@2x.png)
## Do not get panic just yet!

I bet you could have a feeling that being cheated because you still have to manage a key to use all your other keys. Sounds like you get a higher risk than before.

Do not worry, let me explain.

The Gluon password is not the single way of authentication. You can (and you should) config your security settings to add 2FA or 3FA to your Gluon account.

Because Gluon is built on top of the TEA project, a so-called “layer-2” solution framework. It can easily be integrated with other modern authentication solutions like OTP, Hardware Authenticator, Bio-ID, etc.

When you use Gluon to sign a transaction, based on your reconfiguration, you will be asked to punch your additional authenticator’s one-time passkey, face recognization, fingerprint, voice recognization, etc.

![](../res/blog/WX20201215-105650@2x.png)

Those methods are also used for your Gluon master key recovery along with social recovery. Social recovery means you can preset a few family or friends' accounts. When you lost your Gluon key, you can physically ask them to group sign a transaction to recover your account key.

All these authentication or recovery are not done in a traditional centralized way. They are handled in blockchain in a decentralized manner. No one can control or force recover your account, even government enforcement.

![](../res/blog/WX20201215-105927@2x.png)

## Are there actually hardware wallets running in Gluon?

Internally, we do not call them hardware wallets, we call them TEA nodes. We use hardware wallets because it is a common marketing term that everyone understands. Technically TEA node becomes a hardware wallet when the Gluon actor(program) is loaded into it. It is a hardware protected security module (HSM) which the same as hardware wallets.

## TEA nodes do not work alone, they work together

The major difference is that TEA nodes cannot work alone, they can only work together with many other TEA nodes to get consensuses on almost everything. Because there are a lot of TEA nodes running 24X7 on the Peer-to-peer network, you can always get your services as you need. Any single TEA node may hold a small portion of your secret that cannot be recovered without consensus with other TEA nodes, so even they are offline, stolen, burned, or hacked, you won’t lose your secret. This is the methodology of blockchain.

## In what situation, Gluon can get hacked?
There is no 100% security when you still need a little usability and performance. Just like any Blockchain project, Gluon and other TEA projects can be hacked too. But only under the following condition: (assuming Shamir (k,n) algorithm k = 70, n=100)

- Among thousands of TEA nodes (there might be more, let’s assume we have thousands), there are 100 undetermined nodes each holds 1/100 of your private key.

- Hacker happens to hack into 70 TEA nodes of those 100 at the same time and not detected by TEA’s hardware remote attestation consensus

Because the TEA node is a black-box to everyone. No one knows which 100 block boxes among the thousands hold your secret. Hacking into any single hardware protected TEA node is not an easy job, let along there are many different technical stacks used by each TEA nodes. Hackers have to use different tools in every case. It has to be completed successfully in a rather short period of time as the key rotation over time while constant remote attestation may detect the intrusion after a few seconds. I cannot say it is impossible, but I can tell it is very hard and very expensive. As long as it is harder than hacking into your own computer or smartphone, or your hardware wallet, the Gluon is a better choice. right?

## Where to get more information about Gluon?

I am working on a separate Gluon Wallet project from the main TEA project website. In the meantime, you can get the basic information from TEA project website: teaproject.org, or the Framework T-rust from t-rust.com. They are actually what Gluon will be running on. Gluon is an application of the T-rust framework by the TEA project team to demonstrate what TEA can do. So if you understand TEA, you would understand Gluon.

The future Gluon Wallet website will be gluonwallet.com. I hope to get it to work in a few weeks. Please stay tuned.

![](../res/bear3.png)
