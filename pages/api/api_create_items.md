---
title:  Create items (NFTs, Phygitals)
keywords: NFT, graphql
sidebar: api_sidebar
permalink: api_create_items.html
tags: [graphql, NFT]
folder: api_
---

## Items (also know as NFTs, Phygitals, Digital IDs)

An item is represented by an NFT on the blockchain and IPFS.

## Creating items 

Items are created from product templates.  Before creating items, you must first create a product template using the Tokenized Asset Manager or calling the *createProduct* mutation using the GraphQL API.  After creating a product template you will have its ID.  You will then use that ID to create item(s) on the blockchain.

Here is and expample GraphQl mutation.

~~~~
mutation {
  createItemsBatch (productId: 19, count: 5, notes: "5 new items") {
    notes
    nfrIds
    transactionResults
    timeStarted
    timeEnded
  }
}
~~~~

Here is an example curl request which will return all items

~~~~
curl --location --request POST 'https://staging.realitems.io/graphql' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjb3VudHJ5IjoiVVNBIiwidXNlcl9uYW1lIjoia2VuQHJlYWxpdGVtcy5vcmciLCJtb2JpbGUiOiIrNTEwOTMyNDkxMSIsImxhc3RfbmFtZSI6Indvb2RydWZmIiwid2FsbGV0cyI6WyIweGY0ZTVFRjdkZTE1NDQ1QmM1NEU2M0FCMmJGZEM0YkJEY2U0MmUxZkIiLCIweDlFRUNBQjRERjEzQjYzMzhBZDYwMzg4MzVlNjFEQTJENDZjMWRDQjAiXSwiYXV0aG9yaXRpZXMiOlsiU1RBTkRBUkRfVVNFUiIsIkFETUlOX1VTRVIiLCJTVVBFUl9VU0VSIl0sImNsaWVudF9pZCI6InJlYWxpdGVtc3N0YWdpbmdjbGllbnRpZCIsImF1ZCI6WyJyZWFsaXRlbXNzdGFnaW5nand0cmVzb3VyY2VpZCJdLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiaWQiOiIyIiwiZXhwIjoxNjE0OTc0Mjg3LCJmaXJzdF9uYW1lIjoia2VuIiwianRpIjoiYTc0MGIyY2YtYWRmOC00MjQ0LWJiMTMtZTdlOGVhODQyZjI1In0.xNuUbl87rN6lCGjuJV5MWpFZR6uG-SYEA4hZv3EFes8' \
--header 'Content-Type: application/json' \
--data-raw '{"query":"mutation {\n  createItemsBatch (productId: 19, count: 5, notes: \"5 new items\") {\n    notes\n    nfrIds\n    transactionResults\n    timeStarted\n    timeEnded\n  }\n}","variables":{"productId":1,"count":1,"quantity":1,"notes":"item created"}}'
~~~~

If the mutation is successful the response will look something like this.

Note: The nfrIds represent the ID of each new item created.

~~~~
{
    "data": {
        "createItemsBatch": {
            "notes": "5 new items",
            "nfrIds": "1777,1778,1779,1780,1781",
            "transactionResults": "{\"message\":\"Successfully created 5 items\"}",
            "timeStarted": "2021-03-04T22:27:04.732Z",
            "timeEnded": "2021-03-04T22:27:18.741Z"
        }
    }
}
~~~~

If the mutation fails (say for insufficient energy) you will see something like this.  
~~~~
{
  "data": {
    "createItemsBatch": {
      "notes": "5 new items",
      "nfrIds": null,
      "transactionResults": "{\"error\":\"request forbidden tx rejected: insufficient energy\\n\"}",
      "timeStarted": "2021-03-04T22:17:53.112Z",
      "timeEnded": "2021-03-04T22:17:59.105Z"
    }
  }
}
~~~~

{% include links.html %}
