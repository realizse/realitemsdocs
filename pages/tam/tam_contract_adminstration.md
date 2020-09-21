---
title: Smart Contract Administration (TAM)
keywords: Administer Smart Contracts 
summary: "Administration of Smart Contracts"
sidebar: tam_sidebar
permalink: tam_contract_administration.html
tags: [tam]
folder: tam_
---

## Smart Contract Administration

There are two types of smart contracts associated with the Real Items system:  

* Items Contract
* Tracking Contract

### The Items Contract

The items contract contains a sequence of the NFRs that make up the Real Items system.  Each NFR (see VIP181 for more info) has a set of attributes such as:

* An owner
* An approver
* A creation time
* The hash of an IPFS document containing the metadata for this NFR

### The Tracking Contract

The tracking contract contains a series of tracking events.  Each tracking event is associated with an NFR in the Items contract.  Each tracking event has a set of attributes such as:

* A timestamp
* An NFR ID
* The hash of an IPFS document containing the metadata for this event

## Managaging Sponsors

The _sponsor_ of the NFR contract is the VeChain account that pays for each transaction.  By default a contract has no sponsors.  This means that each transaction is paid for by the contract's _Master Account_.  A contract can have multiple Sponsors but only one sponsor can pay for transactions at a time.  The Contract Admin tool allows an Administrator to:

* Add sponsors
* Delete sponsors
* Assign the *active* role to a specific sponsor

{% include links.html %}
