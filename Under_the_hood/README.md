# Sources of Truth: Blockchain and Hardware
There are two souces of trust that the TEA project relies on: the blockchain and hardware.

Every node stores their essential data to the blockchain. Based on blockchain's secure nature, the data stored in blockchain is considered trustable. When doing remote attestation, the verifier won't trust anything the testee claims; everything needs to come from either the historical data in blockchain or the hardware signed message. All other decisions are made based on those two sources of truth. 

# There are Three Chains in the TEA Project
The most frequently asked question about the TEA project is if it's really a blockchain project? Well, the simple answer is no it's not. The longer answer is that the TEA project sits on top of a blockchain as a so-called layer-2 solution. But it's not a blockchain itself. The biggest advantage is that TEA won’t compete with any existing blockchain projects, they cooperate instead.

Not only does TEA sit on top of a blockchain, but it includes two other chains that don't exist in any other blockchain projects: a Trust Chain and a Delegation Chain. These 3 chains work together like a sandwich to build the decentralized trust computing network.

![3chains](https://miro.medium.com/max/980/1*mkkpAyQl9Ot4bAET30gO_g.png)

## Blockchain - the Layer-1 Supporter
As I mentioned above, TEA itself is not a blockchain, but it's built on top of blockchain technologies. TEA uses the blockchain as a layer-1 to provide:
- Economic incentives and penalties that shape its token economy.
- Immutable trust information storage such as credit history, key IDs and hashes.
- Block height as a universal clock between TEA nodes.

Continue [reading...](Tea_on_layer1.md)

[[Delegation_chain]]

## Trust Chain - Our Hardware Security Guard

We support 2 trusted hardware solutions, TEE or TPM/HSM. In the case of TEE, the validation is centralized, so no chain is required. In the case of TPM/HSM, a trust chain runs through the entire remote attestation workflow.

Unlike most other layer-2 trusted computing projects, we don't trust pure software solutions and we don't use expensive and unrealistic cryptographic solutions either. We use mature and widely used Trusted Computing technologies, such as TPM / HSM, as our hardware root of trust. We know TPM alone is not secure enough as TPM has many known vulnerabilities. That’s why we insert it between the blockchain and the delegation chain. TPM can be broken, but the potential damage is limited and can be contained.

[[Trust_chain]]
