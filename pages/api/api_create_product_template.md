---
title:  Create product template
keywords: NFT, graphql
sidebar: api_sidebar
permalink: api_create_product_template.html
tags: [graphql]
folder: api_
---

## Product Templates

A Product Template is a JSON document which is persisted on the backend database.  It is used to create items that are then stored on the blockchain. 

## Create a product template 

You must create product templates before you can create items (NFTs, Phygitals) on the blockchain.  The recommened way to create a product template is to log into the Tokenized Asset Manager and create a template using the UI.  Once you have gotten a hang of that, you may wish to automate the process by using the *createProduct* graphql mutation.  After creating a product template you will have its ID.  You will then use that ID to create item(s) on the blockchain.

Here is and example GraphQl mutation.

~~~~
mutation addProduct ($blockchainId: Int!, $companyId: Int!, $componentName: String, $data: String, $maxItems: Int!, $name: String, $publicProduct: Boolean!) {
      addProduct (blockchainId: $blockchainId, companyId: $companyId, componentName: $componentName, data: $data, maxItems: $maxItems, name: $name, publicProduct: $publicProduct) {
        id
      }
    }
~~~~

Here is an example curl call which will create a product 

~~~~
curl --location --request POST 'https://staging.realitems.io/graphql' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjb3VudHJ5IjoiVVNBIiwidXNlcl9uYW1lIjoia2VuQHJlYWxpdGVtcy5vcmciLCJtb2JpbGUiOiIrNTEwOTMyNDkxMSIsImxhc3RfbmFtZSI6Indvb2RydWZmIiwid2FsbGV0cyI6WyIweGY0ZTVFRjdkZTE1NDQ1QmM1NEU2M0FCMmJGZEM0YkJEY2U0MmUxZkIiLCIweDlFRUNBQjRERjEzQjYzMzhBZDYwMzg4MzVlNjFEQTJENDZjMWRDQjAiXSwiYXV0aG9yaXRpZXMiOlsiU1RBTkRBUkRfVVNFUiIsIkFETUlOX1VTRVIiLCJTVVBFUl9VU0VSIl0sImNsaWVudF9pZCI6InJlYWxpdGVtc3N0YWdpbmdjbGllbnRpZCIsImF1ZCI6WyJyZWFsaXRlbXNzdGFnaW5nand0cmVzb3VyY2VpZCJdLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiaWQiOiIyIiwiZXhwIjoxNjE0OTc0Mjg3LCJmaXJzdF9uYW1lIjoia2VuIiwianRpIjoiYTc0MGIyY2YtYWRmOC00MjQ0LWJiMTMtZTdlOGVhODQyZjI1In0.xNuUbl87rN6lCGjuJV5MWpFZR6uG-SYEA4hZv3EFes8' \
--header 'Content-Type: application/json' \
--data-raw '{"query":"mutation addProduct ($blockchainId: Int!, $companyId: Int!, $componentName: String, $data: String, $maxItems: Int!, $name: String, $publicProduct: Boolean!) {\n      addProduct (blockchainId: $blockchainId, companyId: $companyId, componentName: $componentName, data: $data, maxItems: $maxItems, name: $name, publicProduct: $publicProduct) {\n        id\n      }\n    }","variables":{"blockchainId":1,"companyId":"1","componentName":"DefaultProduct","data":"{\"productId\":\"\",\"description\":\"My Description\",\"external_url\":\"\",\"image\":\"https://realitems.org/ipfs/QmeMsz4f8jMQYeU6BYwtT3fMcQRFU2UyJ6pb63sgKdMTjs\",\"name\":\"My Product\",\"component\":\"\",\"attributes\":[{\"trait_type\":\"ProductType\",\"value\":\"merchandise\"},{\"trait_type\":\"Video\",\"value\":\"https://www.youtube.com/embed/x8sNlXIk4lM\"},{\"trait_type\":\"RecyclingManual\",\"value\":\"https://www.wikihow.com/Recycle-Old-Coffee-Mugs\"},{\"trait_type\":\"MadeIn\",\"value\":\"\"},{\"trait_type\":\"Warning\",\"value\":\"\"},{\"trait_type\":\"ProductName\",\"value\":\"My Product\"},{\"trait_type\":\"ProductUrl\",\"value\":\"https://realitems.shop/collections/100-authentic-marketplace\"},{\"trait_type\":\"Music\",\"value\":\"\"},{\"trait_type\":\"FeaturesArray\",\"value\":[\"Ceramic\",\" Dishwasher and microwave safe\",\" includes Real Items NFT\"]},{\"trait_type\":\"SecretMessage\",\"value\":\"Congratulations, you have completed the process and now have a digital copy send to your email.  Please explore the app and send us a picture on twitter @itemsdapp\"},{\"trait_type\":\"CharityDonationRecipient\",\"value\":\"\"},{\"trait_type\":\"CharityDonationAmount\",\"value\":\"\"},{\"trait_type\":\"CharityMessage\",\"value\":\"\"},{\"trait_type\":\"AuthenticMessage\",\"value\":\"\"},{\"trait_type\":\"Notify3rdParty\",\"value\":\"\"},{\"trait_type\":\"IPFSBrandLogo\",\"value\":\"https://realitems.org/ipfs/QmaRW6vYnKfUy6ic6poDqGu9Bz34WsxHTQGscmWx7FDiKQ\"},{\"trait_type\":\"IPFSCertification\",\"value\":\"https://realitems.org/ipfs/QmNeSY9DCQCrM8jHu3eVMMNyDniAEVN69UFwgkkrTdbj6T\"},{\"trait_type\":\"IPFSproductPhoto1\",\"value\":\"https://realitems.org/ipfs/QmeMsz4f8jMQYeU6BYwtT3fMcQRFU2UyJ6pb63sgKdMTjs\"},{\"trait_type\":\"IPFSproductPhoto2\",\"value\":\"https://realitems.org/ipfs/QmZC3pkPUUMdugbx53puNrzrF5er2WervJriAfpebPtCNo\"},{\"trait_type\":\"IPFSproductPhoto3\",\"value\":\"https://realitems.org/ipfs/QmSiXSGuVQeyCv3pqMWW2Q2xTVrMPHU1PUGqnQVaoQ6Aqh\"},{\"trait_type\":\"IPFSproductPhoto4\",\"value\":\"https://realitems.org/ipfs/QmdpftN5kHxnESK3DMzASW64iT9FpcXfvr6AmqUE7Tp8sg\"},{\"trait_type\":\"IPFSproductPhoto5\",\"value\":\"https://realitems.org/ipfs/QmUw2913K7n5L4JEjvFn2FQX1KjJ5nFe4Pqoy94pdfqsnZ\"},{\"trait_type\":\"IPFSproductPhoto6\",\"value\":\"https://realitems.org/ipfs/QmUFgkt3tJ9TToMfZteJyhSwsnVK3AVYSqaLHTPzSd8jX4\"},{\"trait_type\":\"UnitsProduced\",\"value\":1},{\"trait_type\":\"EmailOptional\",\"value\":false}]}","maxItems":1,"name":"My Product","publicProduct":true}}'
~~~~

If the mutation is successful the response will look something like this.

Note: The nfrIds represent the ID of each new item created.

~~~~
{
    "data": {
        "addProduct": {
            "id": 12
        }
    }
}
~~~~

If the mutation fails you will see something like this.  
~~~~
{
    "errors": [
        {
            "message": "Validation error of type UndefinedVariable: Undefined variable companyId @ 'addProduct'",
            "locations": [
                {
                    "line": 3,
                    "column": 59
                }
            ]
        }
    ]
}
~~~~

{% include links.html %}
