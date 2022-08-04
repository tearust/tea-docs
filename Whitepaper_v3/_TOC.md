# General changes from v2
- Proposal: whitepaper v3 becomes more user friendly. Current whitepaper v2 format, which includes all technical details, will become **tech-whitepaper v3** and available to read through a link but won't be the main focus.
- Better narrative connecting the sections
- More use of graphics / consistent style that uses a color pallete (bold text / headers will be different color).

# TOC Whitepaper v3
## 1. Summary
- Problem we're trying to solve (bringing full-speed dApps to the blockchain).
- How we're solving it (overview of our layer2 and the tech behind it).
- Emphasize the benefits of the TEA Project.
- **Portability**: Firefox-vs-OS metaphor, we can run on top of any blockchain we deploy smart contract to.
- **Trust**: TPM / remote attestation. The various actors don't need to trust each other, it's built into the system.
- **Security**: TPM-protected enclaves / private CML (private data stays in the home).
- **Scalability**: Runs on top of blockchain using GPS / non-traditional consensus.
- **Future of Web3**: Decentralized app execution with database layer available / benefits for developers (WASM / similar 3-tier architecture as web 2.0).

## 2. Layer1 <-> Layer2
### 2.1 Layer1
- **Layer1**: emphasize how we use TPM and remote attestation (Proof of Trust data) to ensure execution environment hasn't been tampered with. We don't verify the computation result.
- Describe how layer1 verification of enclaves is done through smart contracts.

### 2.2 Layer2
- **Layer2**: describe node environment on layer2.
- - GPS ordering of transactions / limitless TPS.
- - Layer2 only stores state change in RAM, not the transactions themselves.
- - Layer2 databases:
- - - Strong consistency state machine (GlueSQL).
- - - CRDT eventually-consistent state database (OrbitDB).
- **Layer2**: emphasize full-speed dApps, not smart contracts.
- Briefly describe tech: IPFS/libp2p / WASM / socket communication

### 2.3 Node infrastructure on layer2
- **Nodes on Layer2**: describe the mining nodes that form the infrastructure of our layer2.
- (Mostly) RPi machines with GPS / TPM.
- Running NixOS (modified).
- Zero-knowledge: are chosen to run tasks through VRF, and no miner has any knowledge of what's running inside their node (can't peak inside enclave).

## 3. Token Economy
### 3.1 TEA Token
- Utility token.
- Used for gas.
- Used to pay for TApp usage.
- Briefly discuss staking / locking options designed to support value of TEA token.
- Explanation of block rewards (tentatively paid out from state maintainer taxes).
- Show pre-mine graphic with legend on how the 100M pre-mine is allocated.
- Given pre-mine / block rewards / locking mechanisms already explained, have a brief discussion about token supply with hypothetical forecasts.
- Explain the rate between TEA and computing resourcse. We will calculate the computing resources the app uses and set a price similar to how AWS does. e.g. 1.25TEA per 1M CPU instructions.

### 3.2 The NFTs
#### 3.2.1 State Maintainer Seat Licenses 
- Runs the state machine (formerly A CML).
- Supply determined by DAO vote. First ~2 years will only be run by team and select invitees.
- Explain the state maintainer seat license tokenomics:
- - State maintainer tax (Harberger tax).
- - Explain Harberger tax is necessary because state maintainer licenses are a public good.
- - Collection pool + distribution pool + reserve fund.
- - Interplay with public service rewards and global token dividends.

#### 3.2.2 CML
- Hosts TApps / gives mining privileges (formerly B CML).
- Explain lifespan, other variability as inscribed into the NFT's metadata.
- Explain DAO algorithm limiting supply.
- Explain public services.

#### 3.2.3 Private CML (?)
- Hosts TApps in the home (formerly C CML).
- Discuss about apps travelling to home.
- Discuss total supply / how interested consumers would obtain these.
- Discussion of mining options for homes including TEA boxes.

### 3.3 TApp Tokens
- Each TApp gets own token, supply is governed by bonding curve.

### 3.4 Staking Tokens
#### 3.4.1 (State Machine) Global Tokens
- Earns a share of the state maintainer tax net of public service rewards which have priority.
#### 3.4.2 (Hosting) CML Tokens
- Each individual CML (hosting TApps) will have their own staking token.

### 3.5 State Memory Tokens
- Devs will have to purchase in order to secure space in state memory.
- Will be issued on a bonding curve.

### 3.6 Bonding Curves
- Explain general mechanism of bonding curves.
- Explain why bonding curves were chosen for 1) TApp tokens 2) staking tokens and 3) state memory tokens.

## 4. Ecosystem Development
3-phase rollout:
1. Miners - explain their importance and what incentives they have to participate.
2. Devs - incentivized by ease of migrating to Web3 through TEA (WASM + database + 3-tier architecture), no need to understand blockchain or consensus.
3. Consumers - incentives to curate TApps (as holders of TApp tokens, benefit from  more demand).

