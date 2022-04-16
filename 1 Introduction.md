# 1. Introduction
# What is blockchain?
- Transaction record database that is distributed
- Decentralized (no one entity maintaining it)
- P2P (peer to peer) network


# When Transactions happen
- New transactions are added into a 'ledger' but this ledger is tamper proof
	- Permanently stores data in sequential link of cryptographic links (called blocks)
	- Shared between all member nodes of network
	- Verified and validated
	- Added to the start of the chain
- Peers in a blockchain uses an agreed protocol.

# How data integrity is ensured
- **Integrity** of data is ensured via Crptography hashes and digital signatures.
- Hashes changes when data is tampered with
- Original senders sign data using digital signatures

# How data are organised
- Arranges data into **groups** or **blocks** that are linked or chained together.
- Timeline of data made automatically with accurate timestamp.
- When block is "filled" it is put into the block chain and merged into this timeline.


# Blockchain vs Cryptocurrency

| basis of comparison | blockchain | cryptocurrency | 
| -- | -- | -- |
| Nature | Technology that records transaction | Tools used in virtual exchanges |
| Use | Record transactions | Make payments, investment etc | 
| Value | No monetary value | Have monetary value | 
| Mobility | Cannot be transferred | Can be transferred | 


# Blocks, Nodes & Network
## Blocks 
- A `block` is like aa Ledger page or a record book. 
- Permanently record data existing on the blockchain. 
- Cannot be modified or deleted once it has been published. 
- A `block` records any transaction which have not entered any previous blocks.
- First block (aka Genesis `block`), all confirmed and validated blocks derive from this first block.
- Each `block` is created with an attachment of hash.
- Each `block` has a reference to the last block (creating a chain link)
:important: In theory it is possible to modify all blocks with powerful computer processers, but there is a way that overcomes this called `proof of work`

![[Pasted image 20220416135427.png]]

### What is proof of work?
- 10 mins to determine a `proof of work`.
- Then append a new block to the chain in the bitcoin blockchain architecture.
- `Miners` carry out this procedure, they are special `nodes` within the bitcoin blockchain framework
- As a reward for validating blocks, they get transaction fees from the block as a reward.

## Nodes
- Any device connected to a network of blockchain is defined as a `node`

![[Pasted image 20220416093452.png]]

- Full nodes - Completely implement all blockchain rules. They form the core or network backbone.
- Lightweight nodes - Most nodes are lightweight nodes.


## Network
- Each `node` or device are actually client and a server at the same time. 
- Computer systems are connected to each other over the internet to form a P2P (peer-to-peer) network.


## Proof of work
- Digital Identity is used to verify users
	- private key
	- public key (visible to everyone)

- Authorization (approved mutually) happens before transaction is appended to a block in the chain.
- For public blockchain use - adding a transaction to the chain is made with the help of **consensus**
- Majority of nodes/computers in the network must show consensus that transaction is legitimate
- Rewards and incentives are given to people who posses the computers in the network to verify transactions - `proof of work`

## Concensus
- **Concensus** are mechanisms are protocol make sure all nodes are synchronized with each other
- Some examples are:
> 1. Proof-of-Work (PoW)
> 2. Proof-of-Stake (PoS)
> 3. Delegated Proof-of-Stake (DPoS)
> 4. Proof-of-Importance (PoI)
> 5. Simplified Byzantine Fault Tolerance (SBFT)
> 6. Delegated Byzantine Fault Tolerance (DBFT)
> 7. Practical Byzantine Fault Tolerance (PBFT)
> 8. Proof-of-Elapsed Time (PoET)

:important: In theory, it is possible to hack this if the hacker can **simultaneously control and edit 51%** of the copies of blockchain so that their new copy becomes the majority copy and thefore the agreed upon chain 


## Merkle Tree
- Hash based data structure
- Each leaf node is hash of a data block
- Each non-leaf node is a hash of its offsptring


## Principle of Mining
- Mining is the process of recoding the pending transaction by adding a new Block into the Blockchain through a mathematical puzzle
- Miners get rewarded by receiving new coins of that Blockchain