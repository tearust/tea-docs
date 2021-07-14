# Our Solution: TEA (Trusted Execution and Attestation)

The TEA Project’s goal is to make rich yet decentralized applications (rich dApps) run  across decentralized computing resources at native speed and with the same scalability as traditional cloud computing. It also aims to create an ecosystem in which network maintainers, application developers, and financial contributors can work together autonomously to foster innovation while providing an efficient trusted computing solution.

The TEA platform solves the secure and trusted computation problems with three major components: hardware-based root of trust, multi-layered trust architecture with immutable records of key data, and token design for the security and sustainability of the network.

## The Hardware-based Root-of-Trust

Hardware has been used as a root of trust for many years. Ever since 2006, many new laptops have come with a built-in Trusted Platform Module (TPM) chip embedded in the motherboard. Since July 2016, Microsoft requires TPM2.0 support on all new PCs that run Windows 10. TPM has been the root of trust used by operating systems (OS) of PCs for more than a decade. Most smartphones nowadays have such chips as well. Modern CPUs often use similar enclave technologies too.

Cloud computing platforms have started to provide hardware-based trusted computing services such as Amazon Nitro to clients that require a higher level of confidential computing service. 

The TEA Project is not proposing to reinvent hardware-based trusted computing technologies. Rather, we are leveraging existing secure hardware technologies, such as TPMs, Intel SGX, or Amazon Nitro, and using them to achieve scalable, decentralized and trusted computing, with the help of blockchain technologies. 

Our idea is that if a computation node can be proven to be in good standing based on the information reported by the embedded TPM chip (through remote attestations), and computation will be carried out in its secure enclave, then we can trust the integrity of the node, and that it will protect the confidentiality of the data being processed. To make sure our information about the trustworthiness of each computational node is reliable, we will 1) use multiple trusted nodes to conduct remote attestation of the computation nodes, and 2) store the results of these remote attestations in the blockchain.

To further secure the overall platform, we are introducing additional measures, as described below. 

## Double-layered trust architecture

In both cloud computing and blockchain technologies, there exist a trilemma: one can only achieve two of the following three objectives: scalability, security, and decentralization. Public blockchains such as Bitcoin and Ethereum emphasize decentralization and security, and therefore tend to be weak on scalability. Cloud computing, on the other hand, emphasizes scalability and security, and therefore cannot easily achieve decentralization.

##The Scalability Issue of Blockchain


The TEA Project tackles this trilemma by separating the three concerns into two layers. Each layer can ensure two of the three objectives. By using a secure channel to bind those two layers together, all three objectives can be met, thus creating a decentralized, secure, and scalable environment to run rich dApps. This approach is similar to Ethereum network’s use of Layer 2 technologies to improve scalability.

The foundation of this solution is the hardware root of trust (RoT), which forms the secure channel that binds the two layers. The hardware RoT allows us to run rich dApps securely and efficiently (without the need to run the same application many times to reach consensus). Having many computing nodes with built-in RoT and the proof of their trustworthiness recording on a public blockchain helps us achieve decentralization and security. The hardware RoT is embedded in the computation layer, verified and recorded in immutable ledgers in the blockchain layer.

Finally, to provide this platform to the user community, we introduce an algorithm that would use a random algorithm to select a main computing node to process the customer’s computation task, and lets this selected node to further decompose the task, delegate the sub-tasks to other trusted nodes, and finally aggregate the results together to present to the client.

![](https://lh3.googleusercontent.com/-OD66MgTvUkaih04DMgfdFfAy8PdalAPza1snTZCSGyM4Lq2zEKUZcyjrMt9vKxIfp0J75bMQd9qvJ2dUjPqamyMjbrL8QoCWooQ78QTGeOovCDLDtJ0ipxJjHKduEQztF_oXGIq)

All three layers work together using smart contracts that are governed by the decentralized autonomous organization (DAO) that is established among the participants of the TEA ecosystem, and incentivized by the two tokens that fuels the ecosystem.

## Dual Token Design

Unlike traditional centralized cloud computing service providers, the TEA Project would not own or run any servers. Instead, like Uber, Airbnb, or any blockchain operators, it is not TEA but individual miners who run actual servers. TEA is a DAO consisting of miners, developers, clients, and investors. TEA provides trust-as-a-service (TaaS), and uses tokens to incentivize participation in order to achieve security and sustainability.

The TEA ecosystem needs a utility token to operate. We currently name this utility token $T. It is used to pay gas when running a computation task, or to reward node operators to perform routine tasks such as verifying the trustworthiness of computing nodes. This token can also be staked to a particular computation node in order to indirectly provide evidence of trust of the node, and to share the reward the node would receive after completing a computation task. There are many other potential ways to use this utility token, under the governance of the DAO.

The $T token is a stable token as its value is pegged to the cost of utilizing computing resources. The same number of $T token should always be able to pay for the same amount of computing resources over time. Also, all $T tokens need to be mined. The TEA project would not embed any $T tokens in the genesis block of its blockchain, or air drop any $T tokens.

The TEA project also introduces a non-fungible token (NFT) called Camelia, or CML. Each CML represents a unique right to run a computation node in the TEA network. You need a CML token to activate a computation node and have the node added to the overall TEA network, which enables the node to start earning rewards. One can use $T to acquire a CML, through an auction process. All $T tokens received by auctioning CML will go to the treasury of the DAO, who would then decide to destroy these $T tokens to reduce the number of such tokens in circulation. 

Each CML token has a lifecycle that is pre-defined by the DAO. This makes the overall ecosystem more dynamic, creating new opportunities and retiring aged nodes along the way.
