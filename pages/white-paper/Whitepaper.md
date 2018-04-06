<!-- <h1 style="text-align:center"></h1> -->
<h1 align="center">Krama Intelligent Protocol (KIP) Whitepaper</h1>

![Krama Intelligent Protocol - Logo](/images/logo.png)

<h3 align="center">WORKING DRAFT</h3>
<h4 align="center">Anantha Krishnan <br/> Ganesh Prasad Kumble<br/> Karthik Balasubramanian</h4>
<h3 align="center">KIP FOUNDATION</h3>
<h3 align="center"><a href="mailto:dev@kip.foundation">dev@kip.foundation</a></h3>

**TABLE OF CONTENTS**
  - [Blockchain landscape](#blockchain-landscape)
    - [Background](#background)
    - [Introduction](#introduction)
      - [What is KIP ?](#what-is-kip)
      - [Why KIP ?](#why-kip)
  - [Krama - The new digital order](#krama---the-new-digital-order)
    - [Enter KIP](#enter-kip)
    - [System Overview](#system-overview)
      - [KIP Wallet Account State](#kip-wallet-account-state)
      - [K2K Interaction state transition](#k2k-interaction-state-transition)
      - [T2T Interaction state transition](#t2t-interaction-state-transition)
      - [U2U Interaction state transition](#u2u-interaction-state-transition)
      - [T2K / K2T Interaction state transition](#t2k-k2t-interaction-state-transition)
      - [K2U / U2K Interaction state transition](#k2u-u2k-interaction-state-transition)
      - [T2U / U2T Interaction state transition](#t2u-u2t-interaction-state-transition)
  - [Beyond blockchain](#beyond-blockchain)
    - [Architectural renaissance](#architectural-renaissance)
      - [TDU](#tdu)
      - [Big Data & Cognition](#big-data-cognition)
      - [Scalability](#scalability)
      - [Throughput](#throughput)
      - [Predictable TCO & Finality](#predictable-tco-finality)
    - [Distributed Marketplace](#distributed-marketplace)
    - [Token economy & DEX](#token-economy-dex)
  - [Enterprise adoption](#enterprise-adoption)
    - [Solution models](#solution-models)
    - [Financial models](#financial-models)
    - [Governance models](#governance-models)
  - [Conclusion](#conclusion)
  - [References](#references)
  - [Further Reading](#further-reading)

## Blockchain landscape

### Background

Evolution of business and its underlying processes always encourage technological advancement in computation & storage. This has led the world to roll through significant leaps in technology & the way its perceived globally.

It all started with the computing era in late 50’s and the early 60’s when computers were being used to process mathematical and scientific calculations to improve speed and accuracy. Data was moved from papers to disks and tapes. Traditional business processes were transformed by the help of computers resulting in increased efficiency. Computers increased the productivity of companies by several folds. A lot of companies started in this era wrote software to help businesses and then licensed these software to end users. The unit of value in this computing era was the ‘Product’ and the underlying technology played a very supportive role, although early in its existence.

The introduction of TCP/IP to the world proved to be the fusion of the _"Information Era"_ with the _"Augmentation Era"_, both at individual and institutional levels. TCP/IP allowed the flattening of the world. Anybody with a computer could be connected to other computers around the world and it created an immense opportunity to host services to interact and exchange information with each other. New value driven models moved from being 'product-centric' to 'customer-centric'. The success of most companies was directly proportional to the number of customers the company served. Search engine companies occupied mainstream spotlight as they had the best number of customers using their services. Lots of other start-ups like Amazon, Facebook, Airbnb and Uber were born that leveraged the power of internet to discover & propagate business-driven network effects. But such intermediaries and aggregators influenced everything in the market dynamics as most of the core components driving these models were centralized in the form of entities, both at business and technology levels.

From the _"Information Era"_ where everything is centralised, the world has been moving on to an age where critical components are being decentralised. In contrast to the key driver as 'data' in _"Augmented Era"_, 'Interaction' is the key to driving new values in the hyper connected digital world. Blockchain is the new technological institution that will fundamentally change how we discover, generate & exchange values.

With an inherent nature of insecurity, humans always depended upon trusted intermediaries to lower uncertainty in exchanging values. With the implementation of blockchain technology, we may be able to reduce the dependency on traditional institutions like banks, corporations and governments to reduce uncertainty and exchange value in the digital world. Several blockchain platforms & technologies have been able to find partial success in disintermediating the incumbents that failed to operate better under ethical & performance grounds.

![Generations of blockchain - differenciation table](/images/whitepaper/KIP-Gen_vs_Feat.png)
<p align="center"> <b>Fig 1:</b> Generations of Blockchain <sup><a href="#references">[1][2]</a></sup> </p>

- **Gen 1 Blockchain**

  Bitcoin transactions are based on the UTXO(Unspent Transaction Outputs) model, with each UTXO having a denomination and an owner (defined by a 20-byte address which is essentially a cryptographic public key[1]), that identifies each bitcoin with its own identity with fungible behaviour, i.e., to be able to transfer parts or the whole bitcoin from one wallet to another with a degree of divisibility to identify fractional parts of bitcoin.

  ![Bitcoin State Transition](/images/whitepaper/bitcoin-statetransition.png)
  <p align="center"> <b>Fig 2:</b> Bitcoin State Transition <sup><a href="#references">[1][2]</a></sup></p>
  As depicted in the above figure, the bitcoin transaction is responsible for state changes due to transfer of bitcoins from one wallet to another. Almost all the transactions evolved in this blockchain is user-driven, meaning the transaction was directly signed by the user holding bitcoins in the wallet.


- **Gen 2 Blockchain**

  Ethereum defines its state transition system as a function which formally verifies a few conditions before executing the transactions that could be directly user-driven or a smart automated contract call from the low-level script executed by the EVM(Ethereum Virtual Machine) based on a few logical triggers driven by oracles etc.

  ![Ethereum State Transition](/images/whitepaper/ethereum-statetransition.png)
  <p align="center"> <b>Fig 3:</b> Ethereum State Transition <sup><a href="#references">[2]</a></sup></p>

  Before mining, Ethereum transactions are validated by several factors including signature, balance, sender's nonce count, enough gas balance, & validity of receiving account.

### Introduction

#### What is KIP ?

KIP is a distributed intelligence protocol that creates hybrid cooperative digital mesh by integrating a new business-ready Gen3 blockchain technology, heterogeneous distributed data, trustable cognition and connected devices.

We live in a digitally intensive era, where people and businesses are interacting continually with specific intents to satisfy requirements of mutual gain.
Harnessing value out of such interactions demands tremendous amount of data and advanced models that demand accuracy of the persisted datapoints, yet often arrive at inaccurate results.

Fortunately, Blockchain has uncovered the possibility of persisting univariate timestamped transactions pointing to the occurrence of the event of transactions accurately, but not the intent behind such interactions.
Even though, Blockchain technologies are able to showcase provenance of an asset and its underlying transactions, it has been proven inefficient to persist & manage the multivariate payload directly on the Blockchain, due to its data architectural constraints. This is results in a _"loss of context"_.

The issue of multi-variate persistence was rescued thanks to off-chain data storage mechanisms introduced by IPFS, StorJ, Swarm, SIA etc.. Although storing the payload information pertaining to a transaction had become easier, the ability to reap trusted and meaningful contexts out of such transactions have been seldom possible due to the lack of an environment that facilitates distributed application of multi-variate information vectors on the persisted data.

KIP resolves this issue with an elegant multilateral approach:  
> _**"Truly distributed intelligence empowered by provenance, creating context with multiple vectors - resulting in meaningful business interactions."**_

KFS(Krama File System) ensures data management in a truly distributed manner by replicating the state changes of all data types cryptographically without any conflicts across the network.

TDU information vectors are applied to these data at the point of interaction and builds on existing points(“The TDU points in the KIP wallet).

These resulting data points pertaining to a user, shapes the future interactions backed by combinatorial assertion made by AI models & the counterparties of the historical interactions.

This facilitates businesses to experiment new white spaces and offer incremental value to its existing propositions.

#### Why KIP ?

We are in a digitally connected world where constant interactions are creating networks that have a personality resembling real world human networks. KIP is essentially a cooperative digital mesh that supports creating the digital order. Krama Intelligent Protocol seamlessly brings together Intelligence, Connectedness and Trust (the new ICT!) to create a fundamental digital fabric on which new digital services can be directly built using distributed intelligence.

Challenges of existing blockchain ecosystems:

1. **Lack of value measure**  
  Business transactions in the new digital era struggle to enable new decision making data & actionable insights without hybrid perspectives on the said transactions. This lack in perspectives is henceforth creating a web sphere of low grade data that is not fit for consumption by advanced models. This gives rise to TDU - the Total Digital Utility in KIP that enables application of multiple information vectors right at the time of the interaction, thereby able to capture business values beyond data.

2. **Inadequate support to big data & cognition**  
  Although big data is critical in enhancing various components in the ecosystem ranging from user experience to business models, blockchain is an ineffective and costly medium to persist big data directly. We may have discovered a few external offchain data storage services such as BigchainDB/Ocean Protocol <sup><a href="#references">[4]</a></sup>, IPFS <sup><a href="#references">[5]</a></sup> , StorJ, Swarm, SIA etc..
  However, the mentioned services have failed to deliver a fully mature storage systems capable of serving query requests of heterogeneous forms in a truly inline distributed yet permanent manner without the need of an external token whose value might be subjected to volatility <sup><a href="#references">[5]</a></sup>. KIP addresses this issue with a highly available in-line distributed file system that charges users for off-chain data storage in a consistent & balanced manner with flexible options to permission the data as required.

3. **Partial scale-outs**  
  The Gen1 & Gen2 blockchain platforms have been able to distribute power across all the nodes in their respective networks. The Proof of Work is followed by its demerits of selective absorption & compete, with the ability to gain domination in the entire the network by owning majority of the high-frequency ASICs. The Proof of Stake eliminates the unnecessary need for energy in mining and funnels the power distribution concept of Casper <sup><a href="#references">[6]</a></sup> by allowing all vested actors to be able to bet / bid on the proposed block, but lose the vested assets if malicious in act. However, this approach is haunted by the demonic demerit of capitalism & corroboration between miners/verifying nodes to establish centralized power to mint block with favourable transactions. An abrupt increase in the number of nodes is not practically addressed by these consensus models. KIP resolves this issue using TARA's ability to organize the new & existing nodes in a sentinel manner with minimum intervention.

4. **Inadequate throughput**  
  Both the Gen1 & Gen2 blockchain platforms have been successfully able to distribute the power among the actors with minimal tradeoffs. However, the platforms have become inefficient in supporting enterprise-grade throughput,with its inability to pass hundreds of thousands or millions of transactions per second. Enterprise businesses with broad range of consumer base & variety of users favour platforms that supports 'scale up' model to ensure availability and aggravate the movements of transactions within fraction of seconds. This is unfortunately a failure in existing blockchain ecosystem as there is an inability to classify the nature & interest of each mining/verifying node entity. KIP addresses this issue with the concept of 'Modulated Trust', ably supported by TARA 'state channels' & run by mutually consented consortiums in each vertical of their own.

5. **Gas volatility & Forks**  
  We understand predictable cost of ownership & operation favours any business application to move further step ahead towards blockchain adoption. Although Gen1 blockchain platforms focused on movement of assets in a peer to peer fashion, the Gen2 blockchain platforms targeting 'real-world' scenarios failed to consider the changes in the gas cost in the long term affected by the associated volatility in the market of their own. The dollar equivalent gas-price payable incurred to print a basic welcome text string using a smart contract today, has increased by several folds since its deployment in 2016. This uncertainty in the gas price & political/financial motivations behind forks has discouraged many businesses to deploy critical components, if not the entire application on the blockchain. KIP addresses these uncertainties by hosting a fork-resistant blockchain with self-balancing utilitarian formula for the KIP token - which serves as the universal interface of payment to all services.

## Krama - The new digital order

### Enter KIP

![Krama PoV](/images/whitepaper/KIP-Krama_PoV.png)
<p align="center"> <b>Fig 4:</b> Krama PoV</p>

Bitcoin and the underlying blockchain mechanism are technological homerun. Blockchain gives back the power in the hands of individuals by removing the need of intermediaries to exchange value directly, hence truly enabling decentralized economies and transform tedious processes that involve human interventions that are susceptible to radical thinking.  

Bitcoin was successfully able to decentralize the supply of currency by reward mechanisms.

Bitcoin's limitation to directly facilitate logical operations for means of transfer evolved Ethereum - a platform to develop truly distributed applications.  

However, ethereum failed to address scalability and throughput issues faced by public blockchain network such as the Bitcoin. Also, ethereum has failed to deliver expectations of the enterprise in maintaining stability of the GAS paid in the divisible form of Ethers(ETH). The gas volatility effect across the network makes it inconvenient for the users to continue with their smart contracts.

In real world scenarios, Blockchain must be paired up with other technologies to truly disrupt the landscape for successful adoption.

KIP addresses this challenge by adding context to the blockchain by leveraging IPFS to scale storage-hungry applications, and KIDE for seamless development experience.

Major components encompassing the KIP ecosystem are:

- **diApp:** The distributed intelligent application

- **KIP Service Interface:** Authenticate & relay user requests to managers of all the Krama services mentioned.

- **Krama Identity Services:** Authenticate actors using external sources such as social IDs, Govt. issued IDs, Dev account IDs & Devices.

- **Krama Smart Contract Services:** Manage accounts, facilitate logical operations, manage accessibility, and security.

- **Krama Tokenization Services:** Float, transfer & manage ERC standard tokens by their characteristics.

- **Krama App Services:** Manage various app-generics ranging from PIN Locks, custom UX elements to deep linking messaging etc.

- **Krama File Services:** On-demand CRUD Operations on KFS & external storage realms.

- **Krama Conformity Services:** Manage & monitor device-level attributes to authenticate actors responsible for high-value transactions.

- **Krama Convolution Services:** Recognize physical objects & tag them for accountability in blockchain realm.

- **Krama Media Services:** Facilitate easier off-chain media integration with applications.

- **Krama Reporting Services:** Allow easy plotting various types of graphs & charts across multiple platforms.

- **Krama Cognitive Services:** Allow integration of various intelligence models to trusted source of transaction & state data.

- **Krama Access Services:** Manage contract ownership, lifecycle & network attributes.

- **Krama Network Services:** Relay & manage transactions / state data from heterogenous blockchain & storage realms.

- **Blockchain Realm:** A multiverse connecting heterogenous blockchain environments run by other consortia under wide range of protocols such as Bitcoin, Ethereum, Sawtooth Lake, Iroha, NEO, EOS <sup><a href="#references">[3]</a></sup>  etc.

- **Storage Realm:** A multiverse connecting the KFS(Krama File System) along with external P2P distributed storage services such as IPFS, StorJ etc.

### System Overview

The order is moving from Transactions to Interactions. KIP leverages emergent techniques & mechanism in the blockchain (such as constellation, zk-Snarks etc.), along with other path breaking technologies in storage (such as swarm key, IPFS etc.).  

#### KIP Wallet Account State

![KIP Account State](/images/whitepaper/KIP-Typical_Account_State.png)
<p align="center"> <b>Fig 5:</b> Typical KIP Account's State</p>

As depicted in the figure above, a typical KIP account managed by the user consists of the KIP balance, nonce count for all the transactions signed on behalf of corresponding account, token balance representing the closing balance of number of tokens left, and the TDU points - an array of balances representing a dimension of TDU in the KIP ecosystem based on the user's behaviour.

#### K2K Interaction state transition

![KIP K2K State Transition ](/images/whitepaper/KIP-K2K_State_Transition_System.png)
<p align="center"> <b>Fig 6:</b> A K2K Interaction state transition</p>

The figure depicts a simple 1-way interaction that involves transfer of KIP from one account to another. In this case, one of the colleague is paying up for their lunch paid by one of the other peer. A split in the bill contract could spawn such interactions.

#### T2T Interaction state transition

![KIP T2T State Transition ](/images/whitepaper/KIP-T2T_State_Transition_System.png)
<p align="center"> <b>Fig 7:</b> A T2T Interaction state transition</p>

The figure depicts yet another simple interaction that involves transfer of tokens of some characteristics from one account to another. In this case, there exists a 2-way interaction with transactions exchanging heterogenous tokens at an agreed rate of exchange.

#### U2U Interaction state transition

![KIP U2U State Transition ](/images/whitepaper/KIP-U2U_State_Transition_System.png)
<p align="center"> <b>Fig 8:</b> A U2U Interaction state transition</p>

The figure depicts yet another simple interaction that involves exchange of heterogenous TDU points for service of a specific skill in exchange for privilege to access another service of some arbitrary form. This is an improvement in the Gen3 where non monetary interests can be realized to achieve similar importance & access to services.

#### T2K / K2T Interaction state transition

![KIP K2T2K State Transition ](/images/whitepaper/KIP-K2T2K_State_Transition_System.png)
<p align="center"> <b>Fig 9:</b> A K2T / T2K Interaction state transition</p>

This figure depicts a hybrid 2-way interaction between two users, due to a mutual demand in heterogenous asset classes - the universal `KIP` & app specific token `FEM` . A typical scenario for such transactions apepar in DEX applications & application service billing buffers.

#### K2U / U2K Interaction state transition

![KIP K2U2K State Transition ](/images/whitepaper/KIP-K2U2K_State_Transition_System.png)
<p align="center"> <b>Fig 10:</b> A K2U / U2K Interaction state transition</p>

This figure depicts yet another 2-way hybrid interactions with demand for utility payable by KIP. Other way, there's a mutual demand for KIP tokens for exchange of acceptable TDU points belonging to a certain dimension.
Such interactions occur under social and professional applications built on KIP where the declared attributes can be audited for transparency before harnessing.

#### T2U / U2T Interaction state transition

![KIP T2U2T State Transition ](/images/whitepaper/KIP-T2U2T_State_Transition_System.png)
<p align="center"> <b>Fig 11:</b> A T2U / U2T Interaction state transition</p>

This figure depicts yet another 2-way interaction with mutual demand for heterogenous asset classes - app tokens with specific characteristics needed to access services, & the TDU points in a specific dimension that is transferable and consumed for similar access to service.
Such interactions may occur in bug bounty & marketplace applications where users are willing to crowdsource in exchange for their app tokens.

## Beyond blockchain

### Architectural renaissance

#### TDU

  ![KIP TDU](/images/whitepaper/KIP-TDU.png)
  <p align="center"> <b>Fig 12:</b> TDU - New measure of persistence</p>

  T.D.U. stands for Total Digital Utility. Essentially, TDU is a collective measure of disparate behavior of actors in the KIP ecosystem involved across different types of interaction on multiple diApps.

  TDU plays a major role in transforming existing digital *"transactions"* into *"interactions"* bearing multiple information vectors. This facilitates the developers to explore a whole new arena of business models and whitespace in the coming digital leap.

  TDU isn't a vehicle to merely capture datapoints. It offers a multi-dimensional value environment for all KIP users to leverage their respective interests and abilities to leverage services. (learn more on TDU [here](/pages/tdu/tdu-specs.md))

#### Big Data & Cognition

  ![KIP TDU](/images/whitepaper/Arch-BigData_and_Cognition.png)
  <p align="center"> <b>Fig 13:</b> Big data persistence & Cognition using KFS</p>

  Big data has become an integral part of business processes at various levels of operations. However, emerging platforms have not been able to address the exponential cost of data replication and simply persisting the consensus of the stored data in a fault tolerant manner.  
  KIP differentiates itself in the market by enabling the users to store information on an external storage realm KFS  (Krama File System, an enhanced version of IPFS) that is capable of storing large volumes of various forms of data, yet maintaining the cryptographic state changes of the data.(learn more on big data persistence & AI practices [here](/pages/kfs/kfs-specs.md))

#### Scalability

  ![KIP TDU](/images/whitepaper/Arch-Scalability.png)
  <p align="center"> <b>Fig 14:</b> Dynamic scale-out & sentinel network organization on KIP</p>

  Most business use-cases on several blockchain platforms are seldom scalable. This reflects the nascent stage of blockchain environment we are in. However, KIP spawns a new generation of blockchain solutions on top of its platform for truly scalable solutions.  
  This is made possible by leveraging PBFT <sup><a href="#references">[7]</a></sup> Hardened RAFT to support abrupt changes in the network strength. The deterministic approach encourages businesses to adopt a minimalistic approach to obtain exponential scaling on cost-efficient hardware, thereby contributing to a greener world.(learn more on scalability [here](/pages/tara/tara-specs.md))

#### Throughput

  ![KIP TDU](/images/whitepaper/Arch-Throughput.png)
  <p align="center"> <b>Fig 15:</b> Throughput using Modulated Trust in KIP </p>

  Real-time businesses such as VISA and other retail or commercial payment systems process thousands of transactions per second. This is far from the current state of majority of blockchain protocols. Waiting for a confirmation of a coffee purchase over sale of diamond doesn’t make true sense in day-to-day life.  
  This issue is addressed in KIP by allowing users to choose the level of trust needed to approve of the transaction between the parties. We call it the “modulated trust”. KIP adopts the modulated trust by leveraging TARA <sup><a href="#references">[8]</a></sup> (Ternary Augmented RAFT Architecture) to achieve partial confirmations from nodes designated by the users(we call them as “fast followers”) as well as stakeholders from other regulatory authorities(we call them as “shadow followers”).(learn more on modulated trust [here](/pages/tara/tara-specs.md))

#### Predictable TCO & Finality

  ![KIP TDU](/images/whitepaper/Arch-Gas_Volatility_and_Finality.png)
  <p align="center"> <b>Fig 16:</b> Predictable gas price</p>

  Predictable gas cost & Transaction finality makes sense to business use-cases where assets are represented in some form and certainty is expected on the ownership of such assets. Many public & private blockchain platforms seem to take on this challenge from a game-theory & crypto-economic approach.  
  As a business-centric blockchain, KIP primarily leverages the fact that private and permissioned blockchains can design intricacies to punish bad actors economically and legally to ensure finality on the assets exchanges between users.  
  KIP also introduces “Multi-Tier nodes” to ensure Txn finality & apt gas usage, thereby encouraging the enterprise in adopting KIP for predictable gas cost. (learn more on predictable gas cost [here](/pages/technical-primer/TechnicalPrimer.md))

### Distributed Marketplace

Individual developers and organizations can reap economic benefits by offering diApps and libraries that can be consumed in-turn to develop applications.

![KIP DIO Marketplace](/images/whitepaper/KIP-DIO_Marketplace.png)
<p align="center"> <b>Fig 17:</b> DIO Marketplace</p>

KIP ecosystem offers makers to host their diApps, libraries and datastores, where, the source can be either closed or open-sourced. Both, the diApps & libraries are addressed by the deployed address of respective logical contracts. Validated datastores are addressed by the unique cryptographic hash generated by the KFS registry.

KIP Marketplace is a DIO(Distributed Intelligent Organization) with extraordinary capabilities to reduce capitalistic approach to competition, thereby facilitating a single level of entry for service providers.

### Token economy & DEX

KIP Tokens are an universal interface to all app tokens on the KIP platform and affiliated marketplaces. Developers specify the app token characteristics using Krama Tokenization Services. This is reflected in the token interface smart contract corresponding to the diApp, takes the service usage into account and charge the user for the same.

![KIP Exchange & Buffer mechanism](/images/whitepaper/KIP-Exchange_and_Buffer_mechanism.png)
<p align="center"> <b>Fig 18:</b> KIP Exchange & Buffer Mechanism</p>

KIP stands out from the rest in Tokenization aspects by allowing both buffer & exchange mechanisms, thereby achieving a universal interface that balances the supply demand of app tokens in the digital ecosystem. All app tokens shall be ICO’ed by the entity offering the DIapp solution and integrated with an inline index to address volatility and entry.

KIP also possesses a unique self-balancing utilitarian formula to calculate platform fee and transaction fee for nodes responsible for consensus, and incentivizes the validators’ interests by awarding slice of TDU Scores in the dimensions relevant to trust and economic activities.

![KIP DEX](/images/whitepaper/KIP-DEX.png)
<p align="center"> <b>Fig 19:</b> KIP Internal DEX</p>

DEX has become a dire necessity in any multilateral blockchain ecosystem, where token can be intermittently exchanged between 2 parties, when required, to avail a particular service from a vendor.

KIP shall possess an internal DEX that facilitates the exchange of complimentary tokens. (learn more on DEX working [here](/pages/technical-primer/TechnicalPrimer.md))

## Enterprise adoption

### Solution models

KIP offers comprehensive & flexible solution models that favours accelerated adoption for your organization.

KIP also offers a simplistic approach to moving critical components in the business model to be migrated. Continuation of historic data, wherever applicable,can be handled by KIP File System at a relatively cheaper cost and higher availability. Existing diApps on other blockchain platforms compatible with KIP Migration can also practise the same models. (Learn more on *Historical Data Migration* [here](/pages/technical-primer/TechnicalPrimer.md))

![Enterprise Adoption - Solution model](/images/whitepaper/KIP-Solution_Model.png)  
<p align="center"> <b>Fig 20:</b> Enterprise Adoption - Solution Model</p>

As represented in the figure above, developers can pick up the specifications based on the organization's strategy & be able to convert them into functional logic in code. This is made possible by KIDE(Krama Integrated Development Environment) - A web IDE that offers seamless environment for development, testing & simulation by providing standard 'consumable' libraries that enables the developer to identify, authenticate and manage actors in a diApp space. KIDE is tightly coupled with all the Krama Services such as Identity Services, Krama Tokenization Services, etc. that are subscribed by the developer's organization. (Learn more on *KIDE* [here](/pages/kide/kide-specs.md))

This resulted diApp(distributed intelligent application) is an instance of the code deployed either on KIP's `test-net` or `main-net` by paying a platform fee based on the tier of the nodes used to verify the contract's initiation, inherently a transaction. (Learn more on *Platform Fee* [here](/pages/technical-primer/TechnicalPrimer.md))

diApps developed on KIP shall be upgrade-able, highly available, secure, and scalable along with user-interactive mechanisms to facilitate feedbacks / iterations.

### Financial models

KIP offers a truly decentralized fashion of monetizing assets and solutions in the form of user's subscription to diApp services at a beneficial cost to both parties with lower and predicable interaction fee.

![Enterprise Adoption - Financial model](/images/whitepaper/KIP-Financial_Model.png)  
<p align="center"> <b>Fig 21:</b> Enterprise Adoption - Financial Model</p>

As depicted in the figure above, developers can float tokens by specifying the nature of the tokens along based on the organization's strategy. This is essentially reflected in a smart contract that spawns tokens in the ecosystem. The characteristics and interface to the tokens are specified in KIDE which is tightly coupled with the Krama Tokenization Service(Learn more on *Krama Tokenization Service* [here](/pages/technical-primer/TechnicalPrimer.md)).

The tokens are integrated to diApps by reference to an address - the adddress of the smart contract deployed through KIDE. This allows the users to spend the tokens to access wide range of services offered by the diApp. Such tokens are used to avail services in the ecosystem and hence treated as *utility tokens*.

The entry to purchase such utility tokens is made possible by DEX(Decentralized Exchange) , an special escrow-like contract run by interested parties to exchange complimentary tokens at a desirable rate and a fee. Users buy relevant tokens necessary by either paying in KIP tokens or by trading one of their other utility tokens. The exchange transactions are mostly immediate, thereby eliminating the synchronous manual efforts needed by the users in comparison to other platforms.

### Governance models

As an enterprise-focused ecosystem, KIP ensures behavioral certainty in the network to the best level possible for frictionless service.

Entities willing to participate as validating nodes in the KIP network need to pass an benchmark / entry test as an onboarding criteria, thereby ensuring a predicted performance before reflecting the KIP's network strength.

Users holding KIP token for a pre-determined amount of time are eligible for vote to changes in the network. This and a set of other criteria ensures the best of interest from users in the ecosystem and reflects the collective responsibility of upholding the network's stability.

![Enterprise Adoption - Governance model](/images/whitepaper/KIP-Governance_Model.png)  
<p align="center"> <b>Fig 22:</b> Enterprise Adoption - Governance Model</p>

As depicted in the figure above, Users and eligible voters are notified of significant breaking changes that are proposed in the upcoming upgrade of the network. Each voter casts a vote on individual breaking changes with either a 'yay', 'nay' or 'abstain'. Votes pertaining to each breaking change is collected in the *voting booth diApp* and verified. Dependency check is conducted internally on the breaking changes to prevent issues with upgrades when a change is implemented without it's supported dependency feature.

Results are calculated based on the epoch and majority rule inscripted into the *voting booth diApp* , allowing customization wherever required.
The results once computed are published on all relevant channels.
KIP platform shall also equip modern OTA-like patch automation mechanisms to fully decentralize the efforts of changes, driven by multi-sig to ensure proper distribution of power. (Learn more on *breaking changes & release management* [here](/pages/technical-primer/TechnicalPrimer.md)).

## Conclusion

KIP establishes distributed intelligence with big data persistence, scalability, maximized throughput, & predictable TCO. This enables enterprises to adopt diApps (distributed intelligent apps) for modern “real-world” scenarios that exhibits Upgradability, Agility, Robustness, Security, Scalability, Responsiveness & Accountability.

## References

\[1\] Satoshi Nakamoto. “Bitcoin: A Peer-to-Peer Electronic Cash System.” 2008; https://bitcoin.org/bitcoin.pdf

\[2\] Vitalik Buterin. “A next generation smart contract & decentralized application platform” 2013; https://github.com/ethereum/wiki/wiki/White-Paper  

\[3\] Daniel Larimer et al. . "EOS Technical Whitepaper" 2017;
https://github.com/EOSIO/Documentation/blob/master/TechnicalWhitePaper.md

\[4\] Ocean Protocol Foundation. “Ocean Protocol: A Decentralized Substrate for AI Data & Services” 2018; https://oceanprotocol.com/tech-whitepaper.pdf

\[5\] Protocol Labs. “Filecoin: A Decentralized Storage Network” 2017; https://filecoin.io/filecoin.pdf

\[6\] Vlad Zamfir. “Introducing Casper “the Friendly Ghost”” 2015; https://blog.ethereum.org/2015/08/01/introducing-casper-friendly-ghost/

\[7\] Castro, Miguel, and Barbara Liskov. “Practical Byzantine Fault Tolerance.” SDI. Vol. 99. 1999; http://pmg.csail.mit.edu/papers/osdi99.pdf

\[8\] Ganesh Prasad Kumble. “TARA: Ternary Augmented Raft Architecture” 2017; https://github.com/TARAFramework/docs/blob/master/TARA.pdf

## Further Reading

1. [KIP Blog](https://medium.com/kipfoundation/)
