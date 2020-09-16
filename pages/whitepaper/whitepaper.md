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

A mutually agreed upon single source of truth in any ***product life cycle*** would allow stakeholders to bypass costly trust-building processes and thus increase efficiency and reduce costs. A technology that uses cryptographic digital signatures to create irrefutable and universally accepted digital identities which are paired to real-world items, would increase transaparency and empower stakeholders to make quicker and more intelligent decisions. By establishing a consenus about the state of an item, friction is reduced and time-consuming, error-prone processes can be removed, optimized, or automated.  The benefits of digital proofs extends far beyond merely improving existing processes. When a stakeholder has instant access to the real-time attributes of an item, such as provenance, shipping history, location, custody, and ownership, new value-add services and industries can be created.

## Digital Identities/Digital Events

Central to our technology is the concept of the ***digital identity***. An item begins its journey when a digital identity is created and assigned to that item.  As an item makes its way through the manufacturing, logistics, sales, and end-use journey, each real-world event is recorded as an attestation which is associated with its digital identity.  Since all stakeholders have instant access to these attestations, real-time analytics can be performed allowing for confident, intelligent, and timely decisions to be made.  The concept of a digital identity combined with an irrefutable digital history creates a trust and transparency that can be leveraged to create new levels of consumer confidence and new channels of revenue generation. 

![Digital Identity](whitepaper_digital_ids.svg){:class="img-responsive"}

##  Creating opportunities 

The benefits of digital identity and digital events on the existing product life cycle are clear, but what if an organization could extend the _product life cycle_ into new territory?  We believe the life of a product does not end when the item enters the hands of consumer. We see end-user engagement as an untapped opportunity in an item's product life cycle.  After an item is delivered to an end-user the user immediately begins interacting with it.  A platform that captures each interaction and allows analysis of the resulting dataset would create new opportunities.  A platform that encourages and enhances user engagement would create even more opportunities.

## Our toolset

Each component of our toolset focuses on moving an item through each step of its life cycle.  For each step in the lifecycle, we provide a tool to achieve that goal. While we provide tools to manually acheive each goal, we also provide integration points which enable the automation of each step.  For example, the creation of a digital identy can be manual or automated, depending on the needs of the organization.  Automation would enable in-house or third-party processes to trigger the creation of a new digital identity. After a digital identity is created, our toolset facilitates the creation of digital events and the association of those events with the digital identity.  This process can be manual or automated.  Our integration points lay the foundation for the use of IOT devices to bolster the history of an item.  

## Architecture - Simplified

Our architecture can be divided into roughly three layers:

* Client Layer
* Business Logic Layer
* Persistence Layer

The Peristence Layer can be further subdivided into 2 sub-layers:

* Mutable
* Immutable

![Architecture Layers](architecture_layers.svg){:class="img-responsive"}

An organization adopting this technology can expect their topology to look like this.  The client layer interact with the system mostly via the Real Items Server.  If the organization decides to become part of the larger Real Items ecosystem, ***Real Items Oracle*** (RIO) will be made aware of this desire and bring it into the ecosystem.

## Barriers to adoption

We have identified 3 major barriers that organizations face when trying to implement consensus-based product life cycle solutions.

1. ***All-or-Nothing Solutions*** - most solutions do not play well with existing ERP systems.  They often require a wholesale replacement of existing solutions and/or the purchase of expensive hardware.
2. ***Crypto-Maximilism*** - most solutions force users to have a deep understanding of cryptoeconomics and force customers to use a proprietary token, a cryptocurrency wallet or both.  This is not only unfair but also unnecessary.
3.  ***Volatile Transaction Costs*** - writing transactions to the Blockchain is not free and the cost of these transactions can be volatile and expensive.  

## Our approach

We have designed and built a system that sidesteps these barriers to adoption.  We have created a system that:

1. Complements rather than replaces a company's existing systems and allows for incremental integration.  An organization can decide which parts of the system are most important to them and integrate them according to their needs and means.  We have designed our system to be flexible enough to run with commodity hardware. 
2. Requires very little understanding of cryptoeconomics and does not force the user to use a proprietary token or a wallet.  We hide the cryptoeconomics as much as possible allowing users to focus on the task at hand.
3. Ensures low and stable transaction costs.  This subject deserves its own section, which is below.

## Keeping Transaction Costs Low and Stable 

One of the biggest challenges for organizations using Distributed Ledger Technology is the cost of gas.  The volatile price of blockchain transactions is a problem that plagues many smart contract platforms - most recently the highly popular Ethereum network.  As the Ethereum platform becomes more popular, the transaction volume increases.  As volume increases so does the valuation of its token, ETH.  Since ETH is used to pay for transactions (in the form of gas), the cost of a given transaction can change rapidly and without warning.  Volatile gas costs can make it difficult for an organization to extrapolate revenue streams. In addition, high prices can make the platform prohibitively expensive for many existing applications.  

Our solution to this problem is two-fold.  

First, we chose a core Blockchain technology that has already solved the transaction cost volatility problem. VeChain solves this by implementing a dual-token system - VET for currency and VTHO for gas. VET is used as the medium of exchange and store of value while VTHO is used to pay for transactions.  These two tokens are loosely-coupled and are controlled by its ***velocity***, the rate at which it is generated from VET.  Unlike Ethereum, the price of the cryptocurrency can rise and fall while transaction costs remain relatively stable.

Second, we have integrated the mechanism of ***fractionalizing*** into our core technology.  Built into our system is ability to construct multiple digital identities from the same ***Non Fungible Record*** (NFR).  For non-durable goods, such as a can of soda or a bottle of ointment, we create a single NFR and then fractionalize it into multiple digital identities.  The number of digital identities derived from the NFR depends on the life span and use of a particular product.

### Whole ###

![Whole](whitepaper_durable.svg){:class="img-responsive"}

### Fractionalized ###

![Batched](whitepaper_batched.svg){:class="img-responsive"}

## Conclusion

We have built a core system which provides a mutually agreed upon single source of truth for a product at any stage in its _product life cycle_.  On top of that we have built a set of tools that allow the various stakeholders to integrate with that system and derive the benefits of real-time knowledge of each stage of a product's life cycle.  Any existing organization that chooses to leverage this knowlege will be empowered with the ability to make intelligent short and long-term decisions regarding its economic relationship with that product.  This newfound ability creates new opportunities within an organization but also creates the opportunity for _new_ industries.


{% include links.html %}
