# Use Cases

## Private Computing

The fundamental capability of the TEA platform is to provide a secure and censorship-free computation service. Users can be assured of the security of the computation nodes, and our commitment to only run the computation in a security enclave. The nodes have no knowledge of the owner of each task, and will provide proof that no residual data remains in the node after the task is completed.

For example, Alice has a collection of family photos she needs to organize. She wants to make sure the computer program will not keep any of the photos and will not try to reveal the identity of anyone in the photos. Bob has developed a program to help index family photos based on time, location, and who are in each photo. Bob wants to get paid for the usage of his application, but doesn’t want anyone to steal his code.

With TEA, Bob would compile his program into Web Assembly code. He would have his code inspected by TEA’s automated tools, and certified to run on TEA. This certified program will be encrypted and stored in TEA’s IPFS storage. 

When Alice’s request comes in, one or more computation nodes will be randomly selected to execute the task. After verification that a computation node is in good standing, the decryption keys for the application code as well as for the photos will be provided to the node(s) so that the program can be run against the photos. The picture below illustrates this process:

![](https://lh4.googleusercontent.com/Q082ER-iuX7jh0uuiE-RuMep0QMkUea7YBoY3PPCPE5aBdw4VqufoZBCl5cq_LepATqayHleOTZNejoskpF8OVBXLh49smEiLVp9_4_JqhYocBkb5g1mNMSoRdm7Hq-3XEGQl_6G)

For the dApp developers, they no longer need to deal with cloud computing service providers. They just compile and deploy their code to the TEA network, and commit a smart contract to the TEA network with information of how payments should be made. Then the developer and the stakeholders will earn $T tokens each time their dApp has been used by clients on the TEA network.

## Gluon

Gluon is the official wallet for TEA, and also a dApp that runs on the TEA network. It has the following features: 

-   Passwordless; users do not need to worry about safely storing the mnemonic phrases.
    
-   Social disaster recovery: help users recover their account even when they have lost all their authentication devices. 
    
-   Private keys over the TEA network are randomly distributed and encrypted by TEA nodes, and the encryption is done inside the hardware-security-modules (HSM) 
    
-   Tolerance of up to 1/3 compromised or failed nodes. 
    
-   Users only need to submit a transaction to Gluon, and the wallet will take over the signing and committing of transactions to the blockchain. 
    
-   Leverages popular biometric technologies in mobile devices to achieve better user experience without compromising security. 
    
The Gluon wallet uses the Schnorr threshold multisignature algorithm to disperse private keys to many TEA enclaves (as shown in the diagram below), but the TEA nodes do not know what they are. Users only need to use Gluon as if it is a typical cloud-based wallet without worrying about security and private keys. If the user’s computer and mobile phone are both lost, the user can still use social recovery to get their assets back.

![](https://lh4.googleusercontent.com/TeDBRTrynx1LoBsCMTNnliFfwduybFcN2ede6He1qBy6KBIv4lQsiZScRWf11piiIq_U7vf87eV_Gd-gxepDaT7xJdZ2ZcjE7OC-vR33nRuWtRDodOGV6Qjt-YlzSSrzCaLA0kw9)

The long-term goal of Gluon is not only a wallet for assets but also an entry point for all kinds of dApps. It will be embedded in TEA’s typical Defi applications so that users can use it as the portal for TEA.

## IPFS Extended

Currently IPFS can only store data or code. If one needs to run the code stored in IPFS, the code needs to be loaded either into a blockchain as a smart contract or a traditional cloud server to execute. The former (smart contract) execution approach is limited by blockchain technologies. The latter (traditional cloud computing) approach falls back to the centralized approach.

Using TEA's solution, we can add a trusted computing module to an existing IPFS node, turn it into a function-as-a-service node. With IPFS extended by TEA, rather than just asking IPFS to download a piece of code identified by the CID, the clients can now ask IPFS (enhanced with TEA modules) to run the piece of code (with or without input parameters) and return the result.

In this scenario, the TEA network will use its verifiable random function (VRF) to select an executor node from nodes that are in good standarding as indicated by attestation data recorded on the blockchain. The TEA network will load the encrypted code to the selected executor, and securely deliver the decryption key to the executor. 

![](https://lh3.googleusercontent.com/RPYD0pEIW8-DGzzXgs-46-Vsvf8O3VIu6Ur6TU3fB7mWYJ5ZBsNMf7sw_F4vn3tcksQuvM3dJVNCXViSFIWFEbIaDuxdv5NkknqGI9qH1mdByuhhxxmctEEi39flrmic6lshl8Yc)

## Edge Computing

We are entering an era of edge computing, in which data is processed closer to where the data source is or where the consumer is, not in the big data centers that tend to be much farther away. 

One concern people have about edge computing is security. Without all the security measures available in a data center, can the computing nodes at edge locations (e.g. cellular towers) be trusted?

TEA can act as a decentralized source of trust that potential consumers can use to verify the PoT of the edge computing nodes. Due to the size and energy consumption requirements, Intel SGX would not be an ideal solution for many edge computing use cases. TPM-based TEA boxes could be a much better fit. 

![](https://lh4.googleusercontent.com/jEpitZ7z_ta3eVhBOUcbwk9AJqpqLwP4K6vavyRXDsAmRukOUkMptUMV2ZZx4GK8hYlkwDUmTXVJmPWbu9l2HcgnT0ZiDK-QGYxLnDy26ymc2HkFLq4eRt295O3uGrfwxlfDjHxF)

With trusted computing empowered by the TEA network, data can be protected right from the IoT sensors that are used to collect the data, at the edge nodes that pre-process the data, all the way to the trusted computing nodes on the TEA network. 

## Trust-as-a-Service for Enterprises 

When enterprises host data and applications to serve its clients, nowadays we want to get a third-party attestation of the service provider’s practices related to infrastructure, data, and application management. These attestations can be in the form of a SOC report, ISO 27001, etc. 

Leveraging the capability offered by the TEA network, organizations can link their computing nodes to TEA, record the proof-of-trust data of its computing nodes in the TEA blockchain, and make such data available to their customers through TEA as an independent trust-as-a-service provider. 

![](https://lh5.googleusercontent.com/K2oKjbqJR4eMgzqivEXRnPcuB3DeYdlqZ-4M79psawKnjpSH1-IzgJbb2cfwqoFp5haj4MRtJcdCKfpUacBx7S1If2_dnT_1wQ8O1C_XCKGgyzKmbypTXOaChJpp6-DPHfO64YEw)

It is conceivable that in the future, customers of such services would only provide encrypted data to the service providers by default. When computation needs to be run on the data, customers would need to see the proof-of-trust information for the computation nodes before releasing the decryption key to such computation nodes. This will provide an extra layer of peace-of-mind for clients who rely on others to process their proprietary data.