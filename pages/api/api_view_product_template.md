---
title: View a product template
keywords: NFT, graphql
sidebar: api_sidebar
permalink: api_view_product_template.html
tags: [graphql]
folder: api_
toc: true
---

## Product Templates

A Product Template is a JSON document which is persisted on the backend database.  It is used to create items that are then stored on the blockchain. 

## View a specific product template using the ID

Here is the GraphQl query

~~~~
query ($id: Int!) {
  productById(id: $id) {
    id
    blockchainId
    companyId
    maxItems
    name
    componentName
    publicProduct
    timeCreated
    timeModified
    data
  }
}
~~~~

Each product template has an ID. Here is an example curl request that uses the ID to return a specific product template.

~~~~
curl --location --request POST 'https://staging.realitems.io/graphql' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjb3VudHJ5IjoiVVNBIiwidXNlcl9uYW1lIjoia2VuQHJlYWxpdGVtcy5vcmciLCJtb2JpbGUiOiIrNTEwOTMyNDkxMSIsImxhc3RfbmFtZSI6Indvb2RydWZmIiwid2FsbGV0cyI6WyIweGY0ZTVFRjdkZTE1NDQ1QmM1NEU2M0FCMmJGZEM0YkJEY2U0MmUxZkIiLCIweDlFRUNBQjRERjEzQjYzMzhBZDYwMzg4MzVlNjFEQTJENDZjMWRDQjAiXSwiYXV0aG9yaXRpZXMiOlsiU1RBTkRBUkRfVVNFUiIsIkFETUlOX1VTRVIiLCJTVVBFUl9VU0VSIl0sImNsaWVudF9pZCI6InJlYWxpdGVtc3N0YWdpbmdjbGllbnRpZCIsImF1ZCI6WyJyZWFsaXRlbXNzdGFnaW5nand0cmVzb3VyY2VpZCJdLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiaWQiOiIyIiwiZXhwIjoxNjE0OTc0Mjg3LCJmaXJzdF9uYW1lIjoia2VuIiwianRpIjoiYTc0MGIyY2YtYWRmOC00MjQ0LWJiMTMtZTdlOGVhODQyZjI1In0.xNuUbl87rN6lCGjuJV5MWpFZR6uG-SYEA4hZv3EFes8' \
--header 'Content-Type: application/json' \
--data-raw '{"query":"query ($id: Int!) {\n  productById(id: $id) {\n    id\n    blockchainId\n    companyId\n    maxItems\n    name\n    componentName\n    publicProduct\n    timeCreated\n    timeModified\n    data\n  }\n}","variables":{"id":1}}'
~~~~

If the request is successful the response will look something like this.

~~~~
{
    "data": {
        "productById": {
            "id": 1,
            "blockchainId": 1,
            "companyId": 1,
            "maxItems": 100,
            "name": "Tricol KN95 Respirator 3 pack",
            "componentName": "DefaultProduct",
            "publicProduct": true,
            "timeCreated": "2020-03-26T03:35:03.345933Z",
            "timeModified": "2020-05-15T19:17:34.823618Z",
            "data": "{\"productId\":1,\"description\":\"Established in 1992, Tricol began as a manufacturer of cotton towels and bedding linens for the global home textile industry. Tricol's presence as a major manufacturer of synthetic textiles began in 1996 with the opening of China's first, and largest, combination microfiber production facility.\",\"external_url\":\"\",\"image\":\"https://realitems.org/ipfs/QmZHPWQsKTtPQZqgXw41Z671c51W1thTMYZMdebZHDa6qz\",\"name\":\"Tricol KN95 Respirator 3 pack\",\"component\":\"DefaultProduct\",\"attributes\":[{\"trait_type\":\"ProductType\",\"value\":\"ppe\"},{\"trait_type\":\"Video\",\"value\":\"https://www.youtube.com/embed/wN7LJt6wWBg\"},{\"trait_type\":\"RecyclingManual\",\"value\":\"https://www.fbi.gov/news/pressrel/press-releases/fbi-warns-health-care-professionals-of-increased-potential-for-fraudulent-sales-of-covid-19-related-medical-equipment\"},{\"trait_type\":\"MadeIn\",\"value\":\"Shandong China\"},{\"trait_type\":\"Warning\",\"value\":\"\"},{\"trait_type\":\"ProductName\",\"value\":\"Tricol KN95 Respirator 3 pack\"},{\"trait_type\":\"Music\",\"value\":\"\"},{\"trait_type\":\"FeaturesArray\",\"value\":[\"Tricol Intelligent Microfiber\",\" silver ion technology\",\" white\",\" earloop\"]},{\"trait_type\":\"SecretMessage\",\"value\":\"This product was verified by Real Items Company securely on VeChain Blockchain. \"},{\"trait_type\":\"CharityDonationRecipient\",\"value\":\"\"},{\"trait_type\":\"CharityDonationAmount\",\"value\":\"\"},{\"trait_type\":\"CharityMessage\",\"value\":\"\"},{\"trait_type\":\"Notify3rdParty\",\"value\":\"\"},{\"trait_type\":\"IPFSBrandLogo\",\"value\":\"https://realitems.org/ipfs/QmQxx52sGAW9gmikgwggsose2ab2NMN73XAsL69a2HtycG\"},{\"trait_type\":\"IPFSCertification\",\"value\":\"https://realitems.org/ipfs/QmcJgUjmkhTfKQ37iPURAM3oNaN9iFciEwTo2PukVws35f\"},{\"trait_type\":\"IPFSproductPhoto1\",\"value\":\"https://realitems.org/ipfs/QmaoRNrQe2C9KjEuNjjPy28EwS7KjYg9MPfKdLCB6oNgvF\"},{\"trait_type\":\"IPFSproductPhoto2\",\"value\":\"https://realitems.org/ipfs/QmQjdBdaL8eQhZfk5SVS4bAX4xkbYs1VB4Q1FiLUcUXTLL\"},{\"trait_type\":\"IPFSproductPhoto3\",\"value\":\"https://realitems.org/ipfs/Qmefu1ok8UU8mGrLtjvXYS9dVoRXp2XsMNMEkigVBtSsFy\"},{\"trait_type\":\"IPFSproductPhoto4\",\"value\":\"https://realitems.org/ipfs/Qmf6k7TqU69J58ujtEBF89rcnjiCv5MRMyuyWrk2SZzskN\"},{\"trait_type\":\"IPFSproductPhoto5\",\"value\":\"https://realitems.org/ipfs/QmafweGoc6QGzswcNUxLU4Sbev7QVaosbkwoXqQoGuQXuw\"},{\"trait_type\":\"IPFSproductPhoto6\",\"value\":\"https://realitems.org/ipfs/QmTLpMeUeyXMFgjfUAUVVNP4aEbfWyGKKETu3xJWLkE1jC\"},{\"trait_type\":\"UnitsProduced\",\"value\":\"100\"}]}"
        }
    }
}
~~~~


{% include links.html %}
