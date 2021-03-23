# Milestone 1  (0 - 3 month)
## Goal
Including:
- Migrate layer 2 tea-runtime and all providers and actors to be running inside AWS Nitro Enclave
- Layer 2 Unit test actors ready for internal testing
- Layer 1 Camellia seed provisioning. It can happen in Polkadot as an ink smart contract instead of the tea-layer1 main chain. This is for seeds presale.
- Presale web portal. Marketing preparation. If we decide not to have a presale, this can be ignored.

Excluding:
- Full feature to interact with Adapter, Facade. These features would be in milestone 2

## Deliverables and task list

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0 | mini-runtime code repo and instruction | Developers can clone and build the mini-runtime that runs inside AWS Nitro virtual machine |
| 1 | mini-runtime test actor and instruction | Testers can use this test actor (the wasm module) to test the existing providers' functionalities |
| 2 | API list of all providers and adapters that supposed to work in AWS Nitro and mini-runtime | including VMH provider, Nitro provider, intercomm-provider, kvp provider, crypto provider, layer1 provider, ipfs-util-adapter, env-util-adapter |
| 3 | Camellia seeds presale web portal | Customers can buy Camellia seeds that can be used for pre-mining in the future. This website is not open to the public until the business model ready |
| 4 | Camellia seeds provisioning in layer 1 | When customers buy a seed, this asset is created on TEA layer 1.  |
| 5 | Gluon wallet shows the Camellia assets in customer's portal | Just for asset ownership purpose not ready for trading in this milestone |
| 6 | TEA Project Technical and Token Economy White paper | |

# Milestone 2 (3 - 6 month)

## Goal

Includes:

- Main net start pre-mining for presale seeds. 
- Gluon integrated miner's portal. 
- Running test dApps in test net. Test miners can get revenue from dApps execution.
- Staking Camellia seeds to other miners. This feature only works in the pre-mining period. It will be disabled when public mining starts.

Excludes:

- Executing dApps in main net
- Token exchange and LMBR. This means the miners can pre-min tokens but not sell them at this moment

## Deliverables and task list

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0 | TEA pre-mining code repo and instruction | Pre-miners can follow the instruction and deploy their own mining nodes for pre-mining. |
| 1 | Gluon upgrade to show the miner's profile | Miners can see their recent mining revenue. the Camellia status and outcome |
| 2 | Code repo for layer 1's Gluon Pellet and Camellia Pellet | Features include Public service mining, customer dApps dispatching (alpha), customer dApps billing (alpha). Camellia staking for pre-mining|
| 3 | Client dApps deployment portal (alpha)| client can upload a sample dApp using the Client portal. |
| 4 | A test net for new features testing | The uncompleted features will be tested in the test net only. Only internal tester or invited beta testers can join |
| 5 | Instruction of deploying client dApps and test mining | This happens in test net only for preview purpose |
| 6 | Sample client's dApps code and instruction | For invited developers only. They can try to build their own customized dApps and deploy them to the test net |

# Milestone 3 (6 - 9 month)
## Goal

Include:

- Staking mining
- General-purpose dApps running on main net
- LMBR protocol (UI)
- Camellia DeX (UI)
- API and documentation for dApps development

Exclude:

- Training material for dApps development
- Special capability dApps
- LMBR and DeX protocols related to other blockchains

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0 | Staking mining code repo | Landlord can invest TEA to other miners as stake |
| 1 | Gluon staking instruction |  Gluon upgrade to show the UI of staking and revenue sharing. Miners can follow the instruction to stake. One release, the Camellia stake feature will be disabled |
| 2 | Upgraded code repo for layer 1's Gluon Pellet and Camellia Pellet | Features includes Staking, Sample clients' dApps |
| 3 | Gluon's LMBR and DeX UI with instruction (alpha) | User can only test LMBR and DeX UI. Not those real features that need to be implemented with other blockchains |
| 4 | API and documentation for client's dApps development (alpha)| For invited developers only. They can learn and follow instruction to build their own customized dApps and deploy to the main net|

