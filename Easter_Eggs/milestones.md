# Milestone 1   
## Goal
Including:
- Migrate layer 2 tea-runtime and all providers and actors to be running inside AWS Nitro Enclave
- Layer 2 Unit test actors ready for internal testing
- Layer 1 Camellia seed provisioning. It can happen in Polkadot as an ink smart contract instead of tea-layer1 main chain. This is for seeds presale.
- Presale web portal. Markcom preparation. If decide not to have a presale, this can be ignored.

Excluding:
- Full feature to interactive with Adapter, Facade. These features would be in milestone 2

## Tasks list

### Layer 1 tasks

#### A1.1 Provisioning Camellia seeds

This can be done out of tea-layer1 blockchain. This is purely for seeds presale. If we decided not to have a seeds presale, we can skip this task. 

It could be an ink smart contract on Polkadot or ERC20 in ETH. The seeds token will be transferred manually to future layer1 main net in genesis block.

### Layer 2 tasks

#### A2.1. runtime client

Runtinme client is a process inside AWS parent instance. It is the module to communicate with enclave using vsock.

- transfer settings for enclave starting
- Vsock Message Hub. Send and receive messages to and from enclave. 
- Handle requests from Adapter and Facade. It is a dummy function at this milestone

### A2.2. Tea-runtime migrates to AWS Nitro

When tea-runtime starts, it connect to runtime client which is outside of enclave. It receives static resources, such as environment var and manifest, loading providers and actors. 

#### A2.3 Update providers to fit both enclave and future TEA Box


| Provider name       | Action | Alternatives         | Notes                                                         |
| ---------- | -------- | -------------- | ------------------------------------------------------------ |
| ipfs       | abundant     | adapter        | There is no network inside enclave. Actors send all IPFS related request to adapter via vsock. Adapter will handle and relay to IPFS nodes in the parent instance |
| env        | abundant     | runtime client | Actors request env from the static resources loaded from runtime client at start|
| intercom   | no change     |                | Intercom can be used as the main communication bus between actors and providers. This is a unix domain socket comm|
| kvp        | minor changes     |                | Only store data in the memory inside enclave. no longer persistent storage feature |
| nats       | abundant     | VMH provider   | There is no network inside enclave. Nats is replaced by VMH (Vsock Message Hub)|
| VMH        | new     |                |   All vsock related message is dispatched using this provider|
| tensorflow | no change     |                | but it only loaded when a Camellia is configured to have Tensorflow feature. Not for all nodes|
| tpm        | abundant     | nitro provider | tpm provider still exists but no longer loaded into enclave since the only way to access the Nitro's tpm is using Nitro provider |
| nitro      | new     | | This provider handles all the security related request to AWS Nitro. This replaces the TPM Provider designed for TEA Box|                                                              |
| crypto     | update     |                | All interface kept the same since they will be reused for TEA Box. The random generator replaced by the Nitro hardware random generator |
| layer1     | new     |                | Load layer1 blockchain global state. This state will be verified by RA actors by running consensus with other enclaves|

nitro、VMH、kvp、intercom provider are included in milestone1. Others complete in milestone2.

#### A2.4.1 layer1 provider

All actors cannot directly query the state from layer1 blockchain. Layer1 provider here become a cache of global state. It query the tea-layer1 node in the parent instance. Load the global state in cached memory so that actors can query latest state. The global state can be verified by RA actor. The RA actor can calculate the hash and compare with the hash with other enclave. If the hash doesn't match for the same block height, one of the enclave is compromised. 

### Actors

Since there is not major changes in actors, no significant tasks for actors at this milestone

# Milestone 2
## Goal
Includes:
- Main net start pre-mining for presale seeds. 
- Gluon integrated miner's portal. 
- Running test dApps in test net. Test miners can get revenue from dApps execution.
- Staking Camellia seeds to other miners. This feature only works in pre-mining period. Will be disabled when public mining starts.

Excludes:
- Executing dApps in main net
- Token exchange and LMBR. This means the miners can pre-min tokens but not sale it at this moment

## Tasks list

### A1.2. Mining for public services

Issue $T for miners who
- Verify block
- RA to other nodes
- Bootstrap services

### A1.3. Mining for clients' tasks

Task dispatching algorithm.
Miners earn reward by their roles in the task. Delegator, Executor, Data owner, Code owner, etc

### A2.4 All remaining providers
There are a few providers not completed in milestone1. They are all done in this milestone.

### Adapter and facade feature complete

### RA complete

# Milestone 3

## Goal
Include:
- Staking mining
- General purpose dApps running on main net
- LMBR protocol
- Camellia DeX
- API and documentation for dApps development
Exclude:
- Training material for dApps development
- Special capability dApps

## Tasks list

### Staking mining

### LMBR protocol

### Upgrade Gluon for all these features UI


# Milestone 4
## Goal
Include:
- IDO public sale
- DAO governance
- Training material, tutorial, sample code of dApps development
- Allow 3rd party capabilities , such as Tensorflow provider
- TEA Box spec

## Tasks list
### Governance voting
- Adjust birth_rate base value.
- Adjust TEA burn rate
- Adjust Camellia NFT specs prepare for new tech stacks (TEA Box, other cloud, SGX etc)
### Developer kits
- Sample code
- Tutorial
- Online training sessions

# Milestone 5
## Goal
- Reference TEA Box testing
- TEA dApps showcase
- Update layer 2 to fit TEA Box

# Milestone 6
##_Goal
- TEA Box beta testing. Invite community members to join the TEA Box testing
- Release TEA Box spec so that others can build their own
- Research on Google Confidential Computing mining instance
- Research on Microsoft Confidential Azure mining instance
