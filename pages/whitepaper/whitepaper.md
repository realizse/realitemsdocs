---
title: Real Items Whitepaper 
keywords: NFR, NFR, Blockchain
summary: "Optimizing and Extending the Product Life Cycle"
sidebar: whitepaper_sidebar
permalink: whitepaper.html
folder: whitepaper_
tags: [whitepaper, tam, cp3, tracker]
---

##  Abstract 

A mutually agreed upon single source of truth in any _product life cycle_ would allow stakeholders to bypass costly trust-building processes and thus increase efficiency and reduce costs. A technology that uses cryptographic digital signatures to create irrefutable and universally accepted digital identities which are paired to real-world items would increase transparency and empower stakeholders to make quicker and more intelligent decisions. By establishing a consenus about the state of an item, friction is reduced and time-consuming, error-prone processes can be removed, optimized, or automated. The benefits of digital proofs extend far beyond merely improving existing processes. When a stakeholder has instant access to the real-time attributes of an item such as provenance, shipping history, location, custody, and ownership, new value-add services and industries can be created.

## Introduction

The Fourth Industrial Revolution, or Industry 4.0, was coined by World Economic Forum Founder Klaus Schwab as the “blurring boundary between the physical and digital world” [1]. Central to our technology is the pairing of a _digital identity_ to a physical item. An item begins its journey when a digital identity is created and assigned to that item. As an item makes its way through the manufacturing, logistics, sales, and consumer journey, each step is recorded as a _digital event_ on the blockchain. Since all stakeholders have instant access to these attestations, real-time analytics allow for confident, intelligent, and timely decisions to be made. The concept of a digital identity combined with an irrefutable history of digital events creates trust and transparency that can be leveraged to create new levels of consumer confidence and new opportunities for revenue generation.

![Digital Identity](whitepaper_digital_ids.svg){:class="img-responsive"}

## Access and Useability

According to worldbank.org, “globally, 1.7 billion adults remain unbanked, yet two-thirds of them own a mobile that could help them access financial services.” [2] 

Real Items technology has kept this fact in perspective, which is why there is no app download required to participate or verify products. Since the unbanked are more likely to buy counterfeit products, it was imperative to provide access through basic mobile.

## Applications 

Here are a few applications that this technology makes possible:

**Verifiable Product Authenticity**

Real Items product lifecycle tracking gives brands the ability to provide their customers with reliable evidence of a product’s makeup including such attributes as raw material source, chemical properties and laboratory test results of input substances, production line assembly and/or treatment processes, time and temp, and any other important event or input. Conscientious consumers enthusiastic about health and well-being, concerned parents, and producers bearing any kind of responsibility or liability for the inputs or ingredients that go into products they bring to market can thereby be completely assured their finished goods are verified authentic.

**A Verified Marketplace**

Counterfeit products are becoming indistinguishable from authentic items, leaving consumers at risk. Traditional ecommerce platforms like eBay, Amazon, Taobao, Alibaba and Flipkart are not able to protect their consumers from counterfeits blending in as authentic. Marketplaces that want to protect customers from fraudulent and untested products need Real Items as their infrastructure to prevent counterfeit products from reaching their listings.

Additionally, the same anti-counterfeit protection provides an on ramp for direct to consumer engagement. The combination strengthens the consumer experience and provides a channel for communication. This gives customer service chatbots more relevance to issues and can assist in registering warranties, sales or insurance.

A live example of this use-case can be found at [Real Items Marketplace](https://realitems.shop/collections/100-authentic-marketplace)

**Decentralized Finance (Defi)**

When enterprises adopt Real Items technology it enables the organization to leverage Decentralized Finance (DeFi) protocols to generate liquidity from their inventory, machinery or accounts receivables. Additionally when end-to-end digitization is matched with stablecoins, it allows organizations to create automated payment incentives that can be executed from real world events and be protected from volatile market conditions (fiat & digital currency).

**Collateralized Commodities**

To collateralize a commodity it requires a verified source for pricing data and condition of the product in its lifecycle. Real Items Oracle provides pricing data for real world assets and the location/phase of the item in its product lifecycle. As the real world asset performs or transfers through the supply-chain, new data is collected and updates the Oracle. Traditional contractual terms can be applied or new experimental terms can be explored.

Types of Assets Protected

Every industry: 
*IoT enabled Devices 
*Heavy Duty Equipment 
*Industrial Machines 
*Transportation Vehicles 
*B2B Accounts Receivable 
*Cargo

**Example Use Case - Heavy Duty Equipment**

A construction company just purchased a fleet of bulldozers worth 20 million dollars. The hours of operation are provided by the machine’s embedded operating system. The company was required to pay for the units in-full and plans to recoup the cost by leasing the units to smaller organizations. With Real Items traceability and DeFi, the construction company will be able to borrow roughly X million dollars by using the portfolio of bulldozers as collateral. To negotiate a better rate or larger amount, the embedded system would report to Real Items Oracle. When a bulldozer is leased, the terms can request repayment in stablecoins(programmable money). With this repayment structure, the lease payments would be automatic and the agreed upon portion of the DeFi loan is repaid in real-time. Once the DeFi loan is paid, the lien of ownership is released and new lease payments are only paid to the construction company.

**Example Use Case - Lettuce Farmer**

A farm that produces lettuce has a straightforward approach to revenue. When the distribution company picks up the harvest, the farmer gets paid. With Real Items, the lettuce would be traceable to the farm that produced it. This tracking creates a historical record of the plant prior to harvested or transported. The lettuce farmer using Real Items tech would be able to provide a record of events that prove the product exists and would be eligible to be approved for a loan on that inventory. This liquidity would come from a DeFi lender or potentially a downstream stakeholder like the distribution company or retailer incentivized by a discount for the real-time payment.

## Architecture - Simplified

Our architecture can be divided into roughly three layers:

* Client Layer
* Business Logic Layer
* Persistence Layer

The Peristence Layer can be further subdivided into 2 sub-layers:

* Mutable
* Immutable

![Architecture Layers](architecture_layers.svg){:class="img-responsive"}

## Components

We provide web and native applications along with API access options to facilitate tracking and tracing items throughout their product life cycle. By leveraging organizations’ existing ERP systems and IOT device infrastructure, our API integrations facilitate product life-cycle event recording automations on blockchain. We also provide a UI suite of tools enabling blockchain interaction when needed.

### TAM (Tokenized Asset Manager)

TAM is a web application that provides the ability to create digital identities for physical items. Once a digital identity is created, TAM is used to manage and monitor those digital IDs. It’s also used to manage the Users, Administrators, and Smart Contracts in a system.

### CP4 (Consumer Protection 4.0)

CP4 is a mobile application that is designed to allow the end-consumer to verify, take ownership, and manage the digital identities of the items they collect. CP4 is a mobile-first web app that requires no installation. After a user verifies and takes ownership of an item, they have access to all of the content and services associated with that item.

### Tracker

Tracker is a mobile application that records tracking events to the blockchain. Tracking information, such as timestamp and location is written to the blockchain and forever associated with an item’s digital identity. This info can also include text, photos, documents, videos and other content.

### RIS (Real Items Server)

The Real Items Server executes the business logic of our platform and handles interaction with the blockchain.

### GraphQL API

We make our GraphQL API available to developers so they can integrate our solution into their existing ERP systems.

### RIO (Real Items Oracle)

The Real Items Oracle is the gateway to the wider Real Items universe and is designed to facilitate visibility of items across the entire real items network, making it a single source of truth for pricing data, lifecycle stage and more.

## Barriers to Adoption

We have identified 4 major barriers faced by organizations that attempt to implement consensus-based product life cycle solutions.

*All-or-Nothing Solutions* - most solutions do not play well with existing ERP systems. They often require a wholesale replacement of existing solutions and/or the purchase of expensive hardware or software.

*Crypto-Maximilism* - most solutions force users to have a deep understanding of cryptoeconomics and force customers to use a proprietary token, a cryptocurrency wallet or both. This is not only counterproductive but also unnecessary.

*Complicated Onboarding* - most solutions require that the end-user download and install software and/or purchase cryptocurrency from an exchange.

*Volatile Transaction Costs* - recording transactions on the blockchain is not free and the cost of these transactions can be volatile and expensive.

## Our Solution 

We have created a system that overcomes these barriers.  Our system:

---

_Complements_ rather than replaces a company’s existing systems and allows for incremental integration. An organization can decide which parts of the system are most important to them and integrate them according to their needs and means. We have designed our system to be flexible enough to run with commodity hardware and software.

---

Requires _very little_ understanding of cryptoeconomics and does not force our customers to use a proprietary token or a wallet. We hide the cryptoeconomics as much as possible allowing users to focus on managing products.

---

_Does not require_ the end-user to install software or purchase cryptocurrency on an exchange.

---

_Ensures low and stable transaction costs_.  This subject deserves its own section, which is below.

One of the biggest challenges for organizations is the _cost of transactions_. The volatile price of blockchain transactions is a problem that plagues many smart contract platforms - most recently the highly popular Ethereum network. As the Ethereum platform becomes more popular, the transaction volume increases. As volume increases so does the valuation of its token, ETH. Since ETH is used to pay for transactions (in the form of gas), the cost of a given transaction can change rapidly and without warning. Volatile gas costs can make it difficult for an organization to predict costs.

Our solution to this problem is two-fold:

_First_, we chose a core blockchain technology that has already solved the transaction cost volatility problem. VeChain solves this by implementing a dual-token system - VET for currency and VTHO for gas. Because the tokens are loosely-coupled, the price of VET can rise and fall while transaction costs remain relatively stable.

_Second_, we have created a mechanism for _fractionalizing_ Non Fungible Records. Built into our system is the ability to construct multiple digital identities from a single NFR. For non-durable goods, such as a can of soda or a bottle of ointment, we can create an NFR and fractionalize it into multiple digital identities.

---

### Whole NFRs

![Whole](whitepaper_durable.svg){:class="img-responsive"}

### Fractionalized NFRs

![Batched](whitepaper_batched.svg){:class="img-responsive"}

## Security

At its lowest level, our technology must guarantee the immutability of each transaction and event written into the system.  We chose a distributed ledger solution that guarantees "absolute finality (or safety guarantee) on blocks and transactions" [3].

All data transmitted between our middleware, clients, and databases is secured by TLS.

All mutable data-at-rest (sql and nosql) is encrypted.  Passwords and other credentials that are not stored in datbases are persisted in a Hashicorp Vault cluster located in a private VPC.

## Conclusion

We have built a system which provides a mutually agreed upon single source of truth for a product at any stage in its product life cycle.  On top of that we have built a set of tools that allow the various stakeholders to integrate with that system and derive the benefits of real-time knowledge of each stage of a product's life cycle.  Any existing organization that chooses to leverage this knowlege will be empowered with the ability to make intelligent short and long-term decisions regarding its economic relationship with that product.  This newfound ability creates new opportunities within an organization but also creates the opportunity for new industries.

## References

[1] Klaus Schwab, "The Fourth Industrial Revolution: what it means, how to respond."  2016. [Online](https://www.weforum.org/agenda/2016/01/the-fourth-industrial-revolution-what-it-means-and-how-to-respond/)

[2] The World Bank, "Financial Inclusion on the Rise, But Gaps Remain, Global Findex Database Shows" 2018. [Online](https://www.worldbank.org/en/news/press-release/2018/04/19/financial-inclusion-on-the-rise-but-gaps-remain-global-findex-database-shows#:~:text=Globally%2C%201.7%20billion%20adults%20remain,help%20them%20access%20financial%20services.&text=It%20adds%20data%20on%20the,150%2C000%20interviews%20around%20the%20world.)

[3] VeChain Foundation, "VeChain Whitepaper 2.0" 2020. [Online](https://www.vechain.org/whitepaper/#bit_65sv8)

{% include links.html %}
