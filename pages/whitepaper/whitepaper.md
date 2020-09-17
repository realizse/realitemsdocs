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

## Introduction

The Fourth Industrial Revolution, or Industry 4.0, was coined by World Economic Forum Founder Klaus Schwab as the “blurring boundary between the physical and digital world” [1].   Central to our technology is the pairing of a ***digital identity*** to a physical item. An item begins its journey when a digital identity is created and assigned to that item.  As an item makes its way through the manufacturing, logistics, sales, and consumer journey, each physical event is paired with a ***digital event*** which is recorded as an attestation on the blockchain.  Since all stakeholders have instant access to these attestations, real-time analytics allow for confident, intelligent, and timely decisions to be made.  The concept of a _digital identity_ combined with an irrefutable history of _digital events_ creates a trust and transparency that can be leveraged to create new levels of consumer confidence and new channels of revenue generation. 

![Digital Identity](whitepaper_digital_ids.svg){:class="img-responsive"}

##  Creating Opportunities 

The benefits of digital identity and digital events on the existing product life cycle are clear, but what if an organization could extend the _product life cycle_ into new territory?  We believe the life of a product does not end when the item enters the hands of consumer. We see end-user engagement as an untapped opportunity in an item's product life cycle.  After an item is delivered to an end-user the user immediately begins interacting with it.  A platform that captures each interaction and allows analysis of the resulting dataset would create new opportunities.  A platform that encourages and enhances user engagement would create even more opportunities.

## An Example Use-Case

**A Verified Marketplace**

An company could use our tools to create a digital identity for each item sold in its e-commerce marketplace.  A user purchases an item and after receiving it in the mail scans the smart label and verify the authenticity of the item.  Then, by taking ownership of the item, the user gains access to all of the content and services associated with that item. Providing content and services for each item they sell, opens many possibilities for continued user-engagement and user analytics.   A live example of this use-case can be found at [Real Items Marketplace](https://realitems.shop/collections/100-authentic-marketplace).

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

Each component of our toolset focuses on moving an item through each step of its life cycle.  For each step in the lifecycle, we provide a tool to achieve that goal. While we provide tools to manually acheive each goal, we also provide integration points which enable the automation of each step.  For example, the creation of a digital identy can be manual or automated, depending on the needs of the organization.  Automation would enable in-house or third-party processes to trigger the creation of a new digital identity. After a digital identity is created, our toolset facilitates the creation of digital events and the association of those events with the digital identity.  This process can be manual or automated.  Our integration points lay the foundation for the use of IOT devices to bolster the history of an item.  

### TAM (Tokenized Asset Manager)

The TAM is a web application that provides the ability to create digital identities for physical items.  Once a digital identitiy is created, TAM is used to manage and monitor those digital IDs. The TAM is also used to manage the Users, Administrators, and Smart Contracts in a system. 

### CP4 (Consumer Protection 4.0)

CP4 is a mobile application that is designed to allow the end-consumer to verify, take ownership, and manage the digital identities of the items they collect.  CP4 is a mobile-first web app that requires no installation.  After a user verifies and takes ownership of an item, they have access to all of the content and services associated with that item.

### Tracker

Tracker is a mobile application that provides the ability to add digital events to digital identities.  When the Tracker scans an items smart label, the user is prompted to provide specific information about the state of the item.  This information, along with the timestamp and location is written to the blockchain as a digital event and forever associated with that digital identity.  Digital events can contain text, photos, documents and videos.

### RIS (Real Items Server)

The Real Items Server manages the business logic and is the gatekeeper between the Real Items system and the blockchain.  Everything that happens to digital identities and digital events goes through the Real Items Server.

### GraphQL API

Interactions with the Real Items Server are handled through the GraphQL API.  In addition to responding to the components of the Real Items system, RIS also serves as an integration point for third-party and in-house applications.  This means that producers can automate existing processes, such as IOT devices, into the creation and management of digital identities and events.

### RIO (Real Items Oracle)

The Real Items Oracle is designed to allow an organization's RI system to communicate with other RI systems.  Via RIO, Digital IDs and events on disparate systems can become visible.  This increases the range of possibilities for end-users and makes it possible to add items to public marketplaces.

## Barriers to Adoption

We have identified 4 major barriers faced by organizations that attempt to implement consensus-based product life cycle solutions.

1. ***All-or-Nothing Solutions*** - most solutions do not play well with existing ERP systems.  They often require a wholesale replacement of existing solutions and/or the purchase of expensive hardware or software.
2. ***Crypto-Maximilism*** - most solutions force users to have a deep understanding of cryptoeconomics and force customers to use a proprietary token, a cryptocurrency wallet or both.  This is not only counterproductive but also unnecessary.
3. ***Complicated Onboarding*** - most solutions require that the end-user download and install software and/or purchase cryptocurrency from an exchange.
4.  ***Volatile Transaction Costs*** - recording transactions on the blockchain is not free and the cost of these transactions can be volatile and expensive.  

## Our Approach

We have designed and built a system that sidesteps these barriers to adoption.  We have created a system that:

_Complements_ rather than replaces a company's existing systems and allows for incremental integration.  An organization can decide which parts of the system are most important to them and integrate them according to their needs and means.  We have designed our system to be flexible enough to run with commodity hardware and software. 

Requires _very little understanding_ of cryptoeconomics and does not force the user to use a proprietary token or a wallet.  We hide the cryptoeconomics as much as possible allowing users to focus on the task at hand.

_Does not require_ the end-user to install software or purchase cryptocurrency on an exchange. 

_Ensures low and stable transaction costs_.  This subject deserves its own section, which is below.


One of the biggest challenges for organizations is the _cost of transactions_.  The volatile price of blockchain transactions is a problem that plagues many smart contract platforms - most recently the highly popular Ethereum network.  As the Ethereum platform becomes more popular, the transaction volume increases.  As volume increases so does the valuation of its token, ETH.  Since ETH is used to pay for transactions (in the form of gas), the cost of a given transaction can change rapidly and without warning.  Volatile gas costs can make it difficult for an organization to extrapolate revenue streams. In addition, high prices can make the platform prohibitively expensive for many existing applications.  

Our solution to this problem is two-fold.  

First, we chose a core Blockchain technology that has already solved the transaction cost volatility problem. VeChain solves this by implementing a dual-token system - VET for currency and VTHO for gas. VET is used as the medium of exchange and store of value while VTHO is used to pay for transactions.  These two tokens are loosely-coupled and are controlled by its ***velocity***, the rate at which it is generated from VET.  Unlike Ethereum, the price of the cryptocurrency can rise and fall while transaction costs remain relatively stable.

Second, we have integrated the mechanism of ***fractionalizing*** into our core technology.  Built into our system is the ability to construct multiple digital identities from the same ***Non Fungible Record*** (NFR).  For non-durable goods, such as a can of soda or a bottle of ointment, we create a single NFR and then fractionalize it into multiple digital identities.  The number of digital identities derived from the NFR depends on the life span and use of a particular product.

### Whole NFRs

![Whole](whitepaper_durable.svg){:class="img-responsive"}

### Fractionalized NFRs

![Batched](whitepaper_batched.svg){:class="img-responsive"}

## Conclusion

We have built a system which provides a mutually agreed upon single source of truth for a product at any stage in its _product life cycle_.  On top of that we have built a set of tools that allow the various stakeholders to integrate with that system and derive the benefits of real-time knowledge of each stage of a product's life cycle.  Any existing organization that chooses to leverage this knowlege will be empowered with the ability to make intelligent short and long-term decisions regarding its economic relationship with that product.  This newfound ability creates new opportunities within an organization but also creates the opportunity for _new_ industries.

## References

[1] Klaus Schwab, "The Fourth Industrial Revolution: what it means, how to respond."  2016. [Online]. https://www.weforum.org/agenda/2016/01/the-fourth-industrial-revolution-what-it-means-and-how-to-respond/


{% include links.html %}
