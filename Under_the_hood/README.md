# Sources of truth: Blockchain and hardware
There are two souces of trust TEA project rely on. The blockchain and hardware.

Every node stores their essential data to the blockchain. Based on blockchain's security nature, the data stored in blockchain is consider trustable. When doing remote attestation, the verifier won't trust anything the testee claims, everything need to come from either the historical data in blockchain or the hardware signed message. All other decisions are made based those two sources of truth. 

# There are three chains in TEA project
The most frequently asked question about TEA project is that “Is it a blockchain project?”. Well, the simple answer is NO. The longer version is that TEA project is on top of a blockchain, it is so-called Layer2 solution. But it is not a blockchain itself. The biggest advantage is TEA won’t compete with any existing blockchain project, they cooperate instead.

Not only TEA sit on top of a blockchain, but also containers other 2 chains that not exists in any blockchain projects: They are Trust Chain and Delegation Chain. These 3 chains work together like a sandwich to build the decentralized trust computing network.
![3chains](https://miro.medium.com/max/980/1*mkkpAyQl9Ot4bAET30gO_g.png)

## Blockchain - the layer1 supporter
As I mentioned above, TEA itself is not a blockchain, but it is built on top of blockchain technologies. TEA uses blockchain as layer1 to provide
- Economical incentive and penalty, token economy.
- Immutable trust information storage, such as credit history, key IDs and Hashes
- Block height as a universal clock between TEA nodes

Continue [reading...](Tea_on_layer1.md)


[[Delegation_chain]]

## Trust chain - our hardware security guard

We support 2 trusted hardware solution, TEE or TPM/HSM. In the case of TEE, the validation is centralized, so no chain is requried. In the case of TPM/HSM, a trust chain run through the whole remote attestation workflow.

Unlikely most other layer2 trusted computing project, we do not trust pure software solution, we do not use expensive and unrealistic cryptographic solution either. We use mature and widely used Trusted Computing technologies, such as TPM / HSM as our hardware root of trust. We know TPM along is not secure enough, there are so much known vulnerabilities of TPM. That’s why we insert it into the bandwidth — between blockchain and delegation chain. TPM can be broken, but the damage is very limited and under control.

Continue [reading...](Trust_chain.md)
