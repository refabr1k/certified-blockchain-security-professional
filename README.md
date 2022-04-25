# Certified Blockchain Security Professional (CBSP) notes

Disclaimer: Content was not created with intention to plagiarize or to illegally distribute the paid course material. These are notes created with the purpose of self-study and revision. Blockchain-council.org maintain the rights to the contents of course found here: https://academy.blockchain-council.org/courses/take/certified-blockchain-security-professional-training

# Table of contents

- [1. Blockchain Basics](#1-blockchain-basics)
  * [What is blockchain?](#what-is-blockchain-)
  * [Value of blockchain](#value-of-blockchain)
  * [When Transactions happen](#when-transactions-happen)
  * [How data integrity is ensured](#how-data-integrity-is-ensured)
  * [How data are organised](#how-data-are-organised)
  * [Blockchain vs Cryptocurrency](#blockchain-vs-cryptocurrency)
  * [Blocks, Nodes & Network](#blocks--nodes---network)
    + [Blocks](#blocks)
    + [Nodes](#nodes)
    + [Network](#network)
  * [What is proof of work?](#what-is-proof-of-work-)
  * [Consensus](#consensus)
    + [Consensus Mechanisms](#consensus-mechanisms)
  * [Merkle Tree](#merkle-tree)
  * [Principle of Mining](#principle-of-mining)
  * [Types of Blockchain](#types-of-blockchain)
    + [Public blockchain](#public-blockchain)
    + [Private blockchain](#private-blockchain)
  * [Fork](#fork)
    + [Hard Fork](#hard-fork)
    + [Soft Fork](#soft-fork)
    + [Hard vs Soft fork](#hard-vs-soft-fork)
- [2. Blockchain Concensus](#2-blockchain-concensus)
  * [What is a concensus algorithm?](#what-is-a-concensus-algorithm-)
  * [Consensus mechanism](#consensus-mechanism)
    + [Public blockchain](#public-blockchain-1)
      - [Proof-of-Work (PoW)](#proof-of-work--pow-)
      - [Proof-of-Stake (PoS)](#proof-of-stake--pos-)
    + [Private blockchain](#private-blockchain-1)
  * [Blockchain Concensus Security](#blockchain-concensus-security)
    + [Proof-of-Work (PoW) Security](#proof-of-work--pow--security)
    + [Security of PoW](#security-of-pow)
    + [51% vulnerability](#51--vulnerability)
    + [Attacking PoW](#attacking-pow)
      - [Double-spending attacks](#double-spending-attacks)
      - [Selfish mining](#selfish-mining)
    + [Proof-of-Stake (PoS)](#proof-of-stake--pos--1)
    + [Security of PoS](#security-of-pos)
    + [Attacking PoS](#attacking-pos)
    + [Double-spending attacks](#double-spending-attacks-1)
  * [Delegated Proof-of-Stake (DPoS)](#delegated-proof-of-stake--dpos-)
    + [Pros](#pros)
    + [Cons](#cons)
  * [Proof-of-Authority (PoA)](#proof-of-authority--poa-)
  * [Proof-of-Burn (PoB)](#proof-of-burn--pob-)
  * [Proof-of-Elapsed Time (PoET)](#proof-of-elapsed-time--poet-)
  * [Byzantine Fault Tolerance (BFT)](#byzantine-fault-tolerance--bft-)
  * [Practical Byzantine Fault Tolerance (PBFT)](#practical-byzantine-fault-tolerance--pbft-)
  * [Direct Acyclic Graphs (DAG)](#direct-acyclic-graphs--dag-)
- [3. Different Security Mechanism](#3-different-security-mechanism)
  * [Public Key Cryptography](#public-key-cryptography)
  * [Basic concepts of Public key cryptography](#basic-concepts-of-public-key-cryptography)
  * [Elliptic Curve Cryptography](#elliptic-curve-cryptography)
  * [Hash Function](#hash-function)
  * [AES (Advanced Encryption Standard)](#aes--advanced-encryption-standard-)
  * [3DES](#3des)
  * [Blowfish](#blowfish)
  * [Twofish](#twofish)
  * [Zero-Knowledge Proofs](#zero-knowledge-proofs)
- [4. Blockchain Risk Considerations](#4-blockchain-risk-considerations)
  * [Risk domains from blockchain](#risk-domains-from-blockchain)
  * [General blockchain risks](#general-blockchain-risks)
  * [Development risks](#development-risks)
  * [Cyber Attack Prevention Strategies](#cyber-attack-prevention-strategies)
- [Block chain architectural design](#block-chain-architectural-design)
  * [Design Process for blockchain-based systems](#design-process-for-blockchain-based-systems)
  * [System Architecture](#system-architecture)
- [5. Two-Factor Authentication (2FA) with Blockchain](#5-two-factor-authentication--2fa--with-blockchain)
  * [Solution Architecture](#solution-architecture)
    + [Ethereum based 2FA architecture](#ethereum-based-2fa-architecture)
- [6. Blockchain Vulnerabilities and Attacks](#6-blockchain-vulnerabilities-and-attacks)
  * [Threat and Vulnerabiltiies Category](#threat-and-vulnerabiltiies-category)
  * [Clients-side Attacks](#clients-side-attacks)
  * [Consensus Mechanism Attacks](#consensus-mechanism-attacks)
  * [Mining Pool Attacks](#mining-pool-attacks)
  * [Network Attacks](#network-attacks)
  * [Smart Contract Attacks](#smart-contract-attacks)
    + [EVM Bytecode Vulnerabilities](#evm-bytecode-vulnerabilities)
    + [Solidity Vulnerabilities](#solidity-vulnerabilities)
- [7. Directed Acyclic Graphs (DAGs)](#7-directed-acyclic-graphs--dags-)
  * [DAGs vs Blockchain](#dags-vs-blockchain)
  * [DAGs benefits](#dags-benefits)
  * [DAGs Challenges](#dags-challenges)


---

# 1. Blockchain Basics
## What is blockchain?
- Transaction record database that is distributed
- Decentralized (no one entity maintaining it)
- P2P (peer to peer) network

## Value of blockchain

![](screens/Pasted%20image%2020220421105915.png)

## When Transactions happen
- New transactions are added into a 'ledger' but this ledger is tamper proof
	- Permanently stores data in sequential link of cryptographic links (called blocks)
	- Shared between all member nodes of network
	- Verified and validated
	- Added to the start of the chain
- Peers in a blockchain uses an agreed protocol.

## How data integrity is ensured
- **Integrity** of data is ensured via Crptography hashes and digital signatures.
- Hashes changes when data is tampered with
- Original senders sign data using digital signatures

## How data are organised
- Arranges data into **groups** or **blocks** that are linked or chained together.
- Timeline of data made automatically with accurate timestamp.
- When block is "filled" it is put into the block chain and merged into this timeline.


## Blockchain vs Cryptocurrency

| basis of comparison | blockchain | cryptocurrency | 
| -- | -- | -- |
| Nature | Technology that records transaction | Tools used in virtual exchanges |
| Use | Record transactions | Make payments, investment etc | 
| Value | No monetary value | Have monetary value | 
| Mobility | Cannot be transferred | Can be transferred | 


## Blocks, Nodes & Network
### Blocks 
- A `block` is like a Ledger page or a record book. 

![](screens/Pasted%20image%2020220416093452.png)

- Permanently record data existing on the blockchain. 
- Cannot be modified or deleted once it has been published. 
- A `block` records any transaction which have not entered any previous blocks.
- First block (aka Genesis `block`), all confirmed and validated blocks derive from this first block.
- Each `block` is created with an attachment of hash.
- Each `block` has a reference to the last block (creating a chain link)
:exclamation: In theory it is possible to modify all blocks with powerful computer processers, but there is a way that overcomes this called `proof of work`

![](screens/Pasted%20image%2020220416135427.png)


### Nodes
- Any device connected to a network of blockchain is defined as a `node`
- Full nodes - Completely implement all blockchain rules. They form the core or network backbone.
- Lightweight nodes - Most nodes are lightweight nodes.


### Network
- Each `node` or device are actually client and a server at the same time. 
- Computer systems are connected to each other over the internet to form a P2P (peer-to-peer) network.

## What is proof of work?
- 10 mins to determine a `proof of work`.
- Then append a new block to the chain in the bitcoin blockchain architecture.
- `Miners` carry out this procedure, they are special `nodes` within the bitcoin blockchain framework
- As a reward for validating blocks, they get transaction fees from the block as a reward.

## Consensus
- Digital Identity is used to verify users
	- private key
	- public key (visible to everyone)
	
- Authorization (approved mutually) happens before transaction is appended to a block in the chain.
- For public blockchain use - adding a transaction to the chain is made with the help of **consensus**
- Majority of nodes/computers in the network must show consensus that transaction is legitimate
- Rewards and incentives are given to people who posses the computers in the network to verify transactions - `proof of work`

### Consensus Mechanisms
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

:exclamation: In theory, it is possible to hack this if the hacker can **simultaneously control and edit 51%** of the copies of blockchain so that their new copy becomes the majority copy and thefore the agreed upon chain 


## Merkle Tree
- Hash based data structure
- Each leaf node is hash of a data block
- Each non-leaf node is a hash of its offsptring

![](screens/Pasted%20image%2020220416144941.png)

## Principle of Mining
- Mining is the process of recoding the pending transaction by adding a new Block into the Blockchain through a mathematical puzzle
- Miners get rewarded by receiving new coins of that Blockchain


## Types of Blockchain
### Public blockchain
- Anyone can read/write without authorization and permission
- More complex rules and consensus algorithm
- Computationally expensive to mine and add a block
- Computational power is distributed globally
- examples: **Bitcoin**, **Ethereum**

### Private blockchain
- Only Authorized node can read/write
- One authorized node can be arbitrator for dispute
- Security is easier as network consists of trusted nodes
- Easy or computationally less expensive to add a Block
- examples: **Hyperledger**, **R3 corda**


## Fork
- Modification to protocol such as when adding new features, fixing security issues
- Chain is split into 2 branches eg. cannot come to a **consensus**
- Two kinds of Forks: Hard Fork, Soft Fork.

### Hard Fork
- Permanent drift - when there is new and updated versions
- Happens when there is enough support from the mining community (90 to 95% support of miners)
- E.g. after an upgrade, the new **consensus protocol** must be used

### Soft Fork
- Soft fork - fork that occur when old network nodes do not follow a rule followed by newly upgraded nodes.
- New rules are followed by old rules will also be honored (backward compatibility)

### Hard vs Soft fork

| | Hard forks | Soft forks | 
| - | - | - |
| **Level** | Work at Protocol level | Work at Network level |  
| **Power** | N.A | Require 50% of hash power |
| **Upgrade** | All nodes and users must upgrade | Do not require all to upgrade | 
| **Split** | Those fail to fork will be split from network | Will not cause a network split | 
| **DAO Attack** | Can return funds without attacker's consent | Cannot retrieve funds from the attacker |


# 2. Blockchain Concensus
## What is a concensus algorithm?
- Provide continuous check on the integrity of both 
	(1) New data blocks
	(2) Past ledger transactions
	
- Rules defined for every blockchain application for generating new blocks:
	(1) Validate legitimacy of new blocks before adding to chain
	(2) Apply to all nodes (aka blockchain's network)
	(3) Processes for validating new blocks of data - written in computer code using algorithms 
	
## Consensus mechanism
### Public blockchain
#### Proof-of-Work (PoW)
- Uses scheme of rewards to encourage users to participate in minding
- Simply "solve puzzles", gain rights and earn rewards for efforts such as fees

#### Proof-of-Stake (PoS)
- Define privileges according to the actual known investment of users

### Private blockchain
Less complex or computer intensive consensus

- **Proof-of-Authority (PoA)**, that verifies the identity of the node
- Simple delegation of authority to those trusted nodes to accept new blocks
- Allow authenticated nodes to publish new blocks at will or rotational basis.

:exclamation: When users on the blockchain do not stick to accepted procedure on the network, the user loses credibility and user's reputation drops, probability of publishing a block also drops. In reality, all this is dynamic and block creation rates can be fast.


## Blockchain Concensus Security
### Proof-of-Work (PoW) Security
- When a block mathematical puzzle is 'solved' by miners, the transactions contained in that block are considered **validated**
- Miners receive some rewards when they solve the complex mathematical problem

![](screens/Pasted%20image%2020220417140152.png)

- In short, the 'maths' problem is distributed to all Generals (Byzantine Generals Problem)
- Solution is integrated to the next PoW problem block.
- Block is created each time a General solves a PoW problem
- A General solves the problem of PoW - everyone elses would eventually solve theirs and know approximately how long it takes for Generals to solve the problem, and if they are still working on the same chain.

### Security of PoW
- Principle that **no entity** should obtain more than 50% of the total hashing or computing power 

### 51% vulnerability
- If an attacker have e.g. 51% of the total hashing power the following can be exploited
> Inject false transactions
> Exploit Blockchain network
> Eliminate all other users from network
> Perform double-spending
> Steal assets from other users

:exclamation: GHash.io alone dominated 54% of the whole BTC network processing power for a day

### Attacking PoW
#### Double-spending attacks
Attacker use same coins to issue two or more transaction, spending More than they actually own. If transaction gets more approval, the less likely the transaction will be reversed in future

#### Selfish mining
Miners raise their porportional mining share by selecting withholding mined blocks and then publishign them progressively. It is possible for an attacker with 33% mining power to use this method to earn 50% of the mining power.

:exclaimation: When all nodes in the blockchain are tightly synchronized, these attacks can be mitigated.

### Proof-of-Stake (PoS)
- Unlike Proof-of-Work, Proof-of-Stake chooses the creator of a new block in a deterministic way (depending on its wealth or stake)

![](screens/Pasted%20image%2020220417141623.png)

- Like PoW, this consensus protocol also seek to address the problem of Byzantine Generals.
- Solutions had been deployed by a few PoS-based networks that avoid **double spending attacks** and other security vulnerabilities that could arise due to Byzantine failures.

:exclamation: Ethereum 2.0 (Senerity) have a PoS algorithm named Casper which allow nodes to achieve consensus with a two-thirds majority before blocks can be formed.

### Security of PoS
- Principle that no entity should obtain more than 50 percent of digital asset

:exclamation: PoS is said to be an safer option for the **51% vulnerability**

Security features:
- **Penalties for attackers:** (1) validator will lose all confidence e.g. to be able to publish a new block (2) Depletion of cryptocurrency valuation - loss of attacker's net worth
- **Barriers to 51 percent stake** (1) buying 51 % stake in one go will have increased difficulty. (2) Coin demand drives up price, making it a very expensive choice.

### Attacking PoS

Similar to PoW

### Double-spending attacks
Attacker use same coins to issue two or more transaction, spending More than they actually own. If transaction gets more approval, the less likely the transaction will be reversed in future

Selfish mining is not possible as there is no reward for miners unlike for PoW. Also, the new PoS Casper protocol impose penalties on malicious actors


## Delegated Proof-of-Stake (DPoS) 

- 3 Groups of people; (1) Consumers (2) Delegates - administer (3) Witness secure network
- Consumers vote for **witnesses** to secure their network
- More tokens one hold = Stronger vote strength e.g Rich are powerful
- If witness are bad, people in community can remove their votes (or fire them)
- Delegates are elected in a manner similar to witness. They administer the network. But can recommend change in size of block or rewards paid by a witness in exchange for validation of a block. Consumers vote whether to implement them.

### Pros
- Strong protection against doublespending
- More democratic, easier to participate in vote (lesser stake held by user)
- More decentralization as more people can particpate (due to low entry threshold)
- Dont need high amounts of power to run network
- Seperates election of block producers from block production
- Provide basis for implementing governance models

### Cons
- Delegators need to be well informed and appoint honest witnesses
- Restricted no of witness can lead to heavy centralization of network
- Vulnerable to weighted voting - smaller stake voters may not take part in voting with possiblity that their "vote wont matter"


## Proof-of-Authority (PoA) 
- Offers high tolerance for performance and faults
- Nodes are authenticated and authroized to create new blocks
- Tolerance to compromised and malicious nodes
- High transactions rate
- Predictable block time

## Proof-of-Burn (PoB)
- Transfer cryptocurrency coins to an address where no one can retrieve
- This protocol is expected to fix issues surrounding energy consumption
- Coins in the address can be viewed by anyone one, but not accessible
- Used by online P2P marketplace OpenBazaar to enable members to execute Credibility Pledges. As they have invested resources on it, these pledges reflect a contribution to an identity on the web.

## Proof-of-Elapsed Time (PoET)
- Designed to improve Proof-of-work
- Alternative for permissioned networks
- Removes the need for mining-intensive process

1) Joining the network and verification
2) Elapsed time, randomized lottery selection process

- Major increase in the performance of proof-of-work protocol

## Byzantine Fault Tolerance (BFT)
- Function of finding an agreement or consensus on individual blocks based on Proof-of-work
- Certain nodes refuse to respond or send out malicious values to misguide the network
- BFT is a way to overcoming these challenges:

(1) Node has technological fault, stops running or responding
(2) Random node failure. Node could fail to return response or respond to a misleading response intentially.

## Practical Byzantine Fault Tolerance (PBFT)
- Idea of finding consensus based on majority of truthful nodes
- Protect against Byzantine fault
- Optimizated for BFT
- Each 'General' manages an ongoing information status
- Consensus is made based on total number of decisions submitted by All the Generals

## Direct Acyclic Graphs (DAG)
- Achieve agreement without Miner's assistance using **Tangle**.
- **Tangle** resolve massive micro-transactions in IoT networks.
- Scalable and TPS are high using Unique Data-Structure
- Output of transaction depends on ability to verify **2 prior transactions**



# 3. Different Security Mechanism
## Public Key Cryptography
- Digital signatures - electronic signed by the **private key** of holder, validated with the **public key** 
- Encryption

## Basic concepts of Public key cryptography
- Authentication
- Non-repudiation
- Integrity
- Confidentiality

## Elliptic Curve Cryptography
- Alternative technique to RSA
- Provides same security as RSA but it is less computer intensive as it uses smaller key sizes

## Hash Function
- Commonly used such as used by bitcoin is SHA-256

## AES (Advanced Encryption Standard)
- AES 128, 192, 256bits with 3 different key weights and each has block 128 bits

![](screens/Pasted%20image%2020220420205820.png)

Different Key sizes have different 'rounds' of encryption mathematical operations

| key size | rounds |
| -- | -- | 
| 128-bit keys | 10 rounds | 
| 192-bit keys | 12 rounds | 
| 256-bit keys | 14 rounds |

\* the more secure the encryption (eg. bigger the key) the more time it takes to encrypt (the trade-off between security and performance)


- Block ciphers, each block is 128 bits long
- 128 bits of cipher text is producted each time 128 bits of plaintext go through the algorithm


## 3DES 
- Not recommended to be used already as it will be deprecated by 2023 by NIST and disallowed from 2024 onwards.
- Considered not secured in modern cryptography

## Blowfish
- Symmetric block cipher
- 8-byte fixed data block size and keys range from 32 to 448bits (4 to 56bytes)
- Considered safe and fast - if keys are large enough to survive a bruteforce attack (at least 16 bytes)

## Twofish
- Symmetric block cipher
- 128-bit block size and accepts a key of up to 256bits.
- Fast and flexible and suitable for network environments where keys are constantly modified
- Suitable environmemts where RAM and ROM are limited or not usable
- 2nd best after AES.


## Zero-Knowledge Proofs
- Without revealing any additional details, one party (prover) may prove that a certain assertion is valid to the other party (verifier)


# 4. Blockchain Risk Considerations

## Risk domains from blockchain
1. Consensus & Network
	> Defective consensus mechanism impact wide spread - e.g. all organizations running on blockchain will be affected by major threats
2. Cryptographic Key management
	> Key pairs not properly maintained
3. Functional requirements
	> Require careful decisions to incorporate a blockchain
4. Smart contracts
	> Programmatically executed
	> Condition based and are executed automatically - error such as unintentionally executing
5. Data management & privacy
	> Any transactions approved by the ledger is final
	> Meaning, incorrect, incomplete or illegal transactions may not be revoked
6. Centralized & Collusion
	> Although blockchain are formed by independent nodes
	> Can potentially be owned by a single entity or organizational partnership - hence centralizing control
7. Interoperability & Integration
	> Risks related to technical issues when blockchain are deployed to legacy IT networks
	> Compatibility restrictions 
8. Scalabilty & Continuity
	> Coordination and interaction between nodes is important for achieving consensus (agreeing on something)
	> Nodes are often isolated and situated in Internal infra (Not public facing and readily accessible)
	> Above will result in loss of scalability or endanger continuity
9. Third Party & Governance
	> Blockchain relys on network of individual and their participating organization's network.
	> Risk may arise not from an individual's environment, but from its third party environments which is not within immediate control.
10. Compliance
	> Goverment policy and regulation are still in implementing and experimenting state
	> Lack of compliance to laws
	> May put risks of organization in risk such as money laundering, funding terrorists

## General blockchain risks
1. Blockchain implementation can be complex
> eg. to transfer data across the "hyper ledger fabric" protocol "Ethereum" protocol. They will require an integration layer to manage both systems.

2. Lack of standardizations
> Too much diversity of frameworks
> Investers have no effective protection against investments

3. Poor valuation value
- Extreme wide swings in crypocurrency values
- May put danger on traders betting on projects

## Development risks

Blockchain is evolving into DLT (Distributed Ledger Technology). **Hyper Ledger** and  **IOTA** make uses of this (and others) and they all pose the same risks:

1. Under developed standards
> No uniformity
> Lack standards for taking up this technology in a way every can follow
> Different versions for different organizations
> Hard to collaborate among organizations
> As such, Risk of security, privacy, interoperability 

2. Different consensus mechnisms
> different consensus have its drawbacks

 3. Data privacy due to different regulations
 > Which privacy law should data adhere to?
 > E.g. EUS privacy only shield transactions between EU and US


## Cyber Attack Prevention Strategies
1. Decrease attack surface - Such as by continous security vulnerability assessment, continously redefining risk assessment scope to be inclusive of all
2. Total Visibility - Understanding current threats and have the latest intel of 0-days and exploitation. Being well informed sets the basis for what to defend against.
3. Prevent risks that are known - Firewall, antivirus, endpoint protection to not defend against common and popular vulnerabilities
4. Prevent risks that are uncertain - Red teaming, studying of intruder techniques, tactics and procedures to be better prepared to respond to such threats

# Block chain architectural design


![](screens/Pasted%20image%2020220423092518.png)


## Design Process for blockchain-based systems

![](screens/Pasted%20image%2020220423093346.png)

Approach begins with the decision to decentralize authority or not.

## System Architecture

![](screens/Pasted%20image%2020220423093531.png)


# 5. Two-Factor Authentication (2FA) with Blockchain

- **Cloud based** - 2FA providers. Typically used extensively for e-commerce, online banking etc
- **On-premise solution** - Using internal VPN integrator who process certificates and shares a key between Internal 2FA providers and third parties. E.g 3rd party 2FA providers can produce OTP and exchange it via sms or mobile apps with employee


## Solution Architecture

Ethereum allows applications (dApps) to  be programmed with a smart contract. Having.

Some companies such as Bit ID have projects that allow users sign up to any service using their unique bitcoin wallet addresses and private keys. Such a platform could be adopted to serve as a 2FA protocol on top of the bitcoin blockchain.

### Ethereum based 2FA architecture

![](screens/Pasted%20image%2020220423123438.png)



![](screens/Pasted%20image%2020220423123616.png)


# 6. Blockchain Vulnerabilities and Attacks

## Threat and Vulnerabiltiies Category
1. Clients-side vulnerabiltiies
2. Consensus mechanism vulnerabilities
3. Mining pool vulnerabilities
4. Network vulnerabilities
5. Smart contract vulnerabilities


## Clients-side Attacks
- **Digital signature vulnerabilities**. Eg. ECC (elliptic curve cryptography) assymetric cryptography which is used by bitcoin. ECC does not have the randomness required which may compromise private key of user. To generate a digital signature, a random value must be used for the private key.
- **Hash function function vulnerabilities** - SHA256 is vulnerable to preimage and collision attacks
- **Mining Malware** - Launch malware on local device or computer to use victim's computer hardware resources to mine block (blockchain).
- **Software's flaws** - Coding related, runtime, concurrency hard fork flaws. E.g. in 2014 during software upgrade, Blockchain.info (hybrid wallet provider) made an error when users create a new key pair - the inputs were not appropriately random which allows an attacker to access public address to compromise the private keys of users.
- **User's Address Vulnerabilities** - identity fraud. Attacker use MITM attack to change the target bitcoin address during transactions


## Consensus Mechanism Attacks

- **51% Attack** - Gaining 51% control of total coins (or hashing power) in the network may allow an attacker to exploit this vulnerability to monitor the entire blockchain network. The attack could potentially inject, manipulate transactions or steal users assets.
- **Alternative History Attack** - Atttacker send to merchant transaction that pays. While also privately mining an alternate blockchain fork (double spending) transaction. If the attacker happen to find More blocks (while waiting) he releases the previous fork to regain his coins. Repeating this to try playing catchup wit the network.
- **Finney attack** - Doublespending attack that is like a race condition attack. E.g. Attacker transfers from A to B (both address he owns). He generates a block but dont broadcast it, but when he makes a payment to C with his address A. When the goods is transfered, he then broadcasts his block and the transaction takes precedence such as mention earlier A pays to B (own money to his pocket) but yet he receives the goods he didnt pay for (from C)
- **Race Attack** - Based on PoW. Attacker makes 2 competing transaction at the exact same time.
- **Vector 76 attack** - Attack idenitified by a user called Vector76 which is based on Double Spending attacks. One-confirmation attack, that makes a transaction with only 1 confirmation can still be reversed. In a successful attack, the attacker will 'sacrifice' one block by not broadcasting it, but instead relay it only to the attacked node. After that, the attacker initiates a transactions that makes a legal deposit into the target adn mines it to the stack.

## Mining Pool Attacks

- **Block WithHolding Attack** - Withhold block to decline the estimated revenue of pool. Aim of attack is to cause mining pool profitability to deline. This is typically possible via the pool administrator who cheats the entire pool.
- **Bribery Attack** - bribing miners using the following 3 types of bribing techniques: (1) **out-of-band payment**, owner of services is paid directly by attacker to mine the blocks of the attacker. (2) Attacker builds a pool in the **negative-fee mining pool** by awarding the higher return. (3) Attacker tries to bribe the blockchain itself using **in-band payment** by making a fork, involves free bribe money to any miner who endorses the fork of the attacker.
- **Pool Hopping Attack** - Based on appeal rate, attacker mines if the rate is high, otherwise, attacker leaves the pool. By gathering intel of the amount of submitted shares in the target, the attacker can maximize full profits and chose seperate pool to mine.
- **Block Discarding Attack** - Attacker must first possess sufficient number of network connection relative to the "honest" nodes. Idea is to improve network dominance by quickly publishes his own block in order to discard blocks of "honest" blocks.
- **Selfish Mining Attack** - Group of attacker conspires to build a mining pool against "honest" miners. Eg. miner withholds a "solution" for a block he mined and continue working on the next "problem" while his peers are still solving the previous block. If lucky, he can find 2 blocks in a row before anyone else does.
- **Fork-After-Withholding Attack** - (FAW) attack is a combination of Block WithHolding attack + Selfish mining attack.  


## Network Attacks
- **Partition Attack** - Attacker isolates group of nodes from rest of the bitcoin blockchain network to break network into disjointed parts. Attacker spoof most of the isolated nodes to redirect the traffic to attacker controlled IP addresses. Attacker can drop packets etc.
- **Delay Attack** - Create delay in block publishing by modifying the content of individual messages (if lack of integrity and encryption checks)
- **Distributed Denial of Service Attack** (DDoS) - These attacks have caused companies such as BitQuick and CoinWallet to shutdown within few months of beginning operations. This is one of the most popular and inexpensive attacks.
- **Sybil Attack** - Attacker setup fake assistant nodes and aims to reveal part of the blockchain network. Goal of attack is that attacker can feed misleading data to victims. This could typically be eploited by attacker disabling the functionality of the concensus algorithm and trigger a possible double-spending attack.
- **Transaction Malleability Attack** - Modify TXID (transaction ID) without revoking the transaction. This is to trick victim into thinking that the transaction failed. eg. Attacker withdraws from an exchange, then with another TXID, republishes the same transaction (one of them appears on the network). But due to the delay, rather than the initial withdrawal, it is likely that the changed transaction will win. The currency exchange will not find the original transaction on the network, and assume that the exchange only depends on TXID. The attacker can continously make withdrawals.

## Smart Contract Attacks
### EVM Bytecode Vulnerabilities
Ethereum virtual machine (EVM) is a bytecode running virtual machine that product of compiling smart contracts source code. GAS is consumed for each process in the EVM and reflects the execution expense of the code.

| Vulnerability Name | Reason | 
| -- | -- |
| Ether lost in transit | Anything sent to an address that is not associated with a user will be lost forever. There is no way to check if the address is orphan or not |
| Immutable bugs | Published smart contracts are immutable against any alteration |
| Stack size limit | Call stack limitation can be leveraged by attackers |


### Solidity Vulnerabilities
Solidity is ethereum's high level programming language. In smart contract source codes, there are 6 documented vulnerabilities that are already exploited:

| Vulnerability Name | Reason | 
| -- | -- |
| Calls to unknown | Fallback function is invoked when calling a function that don't exist | 
| Exception disorder | Anomaly in exceptions handling | 
| Gasless send | Invoking the out-of-gas exception | 
| Keeping secrets | Compromise a private field in the smart contract | 
| Reentrancy | Reenter a non-recursive function before its termination. E.g. 2016 DAO attack | 
| Type casts | No exception is thrown when caller made an error | 

#  7. Directed Acyclic Graphs (DAGs)

DAG protocol is an alternative to standard blockchain or known as distributed ledger technology.

## DAGs vs Blockchain

![](screens/Pasted%20image%2020220425195831.png)


## DAGs benefits
- Scalable 
- Lower user costs
- Suited for high volume transactions, the larger the number of transactions, the earlier they are validated by a DAG
- DAGs eliminates use of miners which means lower energy usage

## DAGs Challenges
- Decrease in transaction volume render DAGs vulnerable to attacks
- replication of data accross nodes is difficult (to solve)
- DAGs employ a 'co-ordinator' to avoid malicious attacks on attacks serving as a centralized, voluntary and temporary alternate consensus mechanism 
:question: Hmm wouldnt that not be de-centralized anymore???