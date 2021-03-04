---
title: List all items 
keywords: NFT, graphql
sidebar: api_sidebar
permalink: api_list_items.html
tags: [graphql, NFT]
folder: api_
---

## Items (also know as NFTs, Phygitals, Digital IDs)

An item is represented by an NFT on the blockchain and IPFS.

## View all items 

Calling this query can potentially return a **HUGE** amount of data. It will be very rare to make this query.  Instead you will probably want to use *itemsByProductId* or *itemById*.  

Here is the GraphQl request.

~~~~
query {
  allItems {
    quantity
    tokenUri
    timeCreated
    timeModified
    id
    obfuscatedId
    approver
    productId
    externalUrl
    stolen
    notes
    owned
    owner
    forSale
    deleted
    metadata
    earmarks
  }
}
~~~~

Here is an example authentication curl request which will return all items

~~~~
curl --location --request POST 'https://staging.realitems.io/graphql' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjb3VudHJ5IjoiVVNBIiwidXNlcl9uYW1lIjoia2VuQHJlYWxpdGVtcy5vcmciLCJtb2JpbGUiOiIrNTEwOTMyNDkxMSIsImxhc3RfbmFtZSI6Indvb2RydWZmIiwid2FsbGV0cyI6WyIweGY0ZTVFRjdkZTE1NDQ1QmM1NEU2M0FCMmJGZEM0YkJEY2U0MmUxZkIiLCIweDlFRUNBQjRERjEzQjYzMzhBZDYwMzg4MzVlNjFEQTJENDZjMWRDQjAiXSwiYXV0aG9yaXRpZXMiOlsiU1RBTkRBUkRfVVNFUiIsIkFETUlOX1VTRVIiLCJTVVBFUl9VU0VSIl0sImNsaWVudF9pZCI6InJlYWxpdGVtc3N0YWdpbmdjbGllbnRpZCIsImF1ZCI6WyJyZWFsaXRlbXNzdGFnaW5nand0cmVzb3VyY2VpZCJdLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiaWQiOiIyIiwiZXhwIjoxNjE0OTc0Mjg3LCJmaXJzdF9uYW1lIjoia2VuIiwianRpIjoiYTc0MGIyY2YtYWRmOC00MjQ0LWJiMTMtZTdlOGVhODQyZjI1In0.xNuUbl87rN6lCGjuJV5MWpFZR6uG-SYEA4hZv3EFes8' \
--header 'Content-Type: application/json' \
--data-raw '{"query":"query {\n  allItems {\n    quantity\n    tokenUri\n    timeCreated\n    timeModified\n    id\n    obfuscatedId\n    approver\n    productId\n    externalUrl\n    stolen\n    notes\n    owned\n    owner\n    forSale\n    deleted\n    metadata\n    earmarks\n  }\n}","variables":{}}'
~~~~

If the request is successful the response will look something like this.

~~~~
{
    "data": {
        "allItems": [
            {
                "quantity": 1,
                "tokenUri": "QmeCECHkcxrX5fhLQEMg3NhzxnEZyfjZJgKBy8Q1qA7io2",
                "timeCreated": "2020-03-26T05:12:55.471767Z",
                "timeModified": "2020-03-26T05:12:55.471767Z",
                "id": 1,
                "obfuscatedId": "Q6Xr6X9Z",
                "approver": "0x74643fa9137b36658378921f2a9917c410d0b118",
                "productId": 1,
                "externalUrl": "https://staging.realitems.io/items/Q6Xr6X9Z",
                "stolen": false,
                "notes": "",
                "owned": false,
                "owner": "0x2437d1acb5fe1ed4caea5b45aac26814b1ffd78b",
                "forSale": false,
                "deleted": false,
                "metadata": "{\"image\":\"https://realitems.org/ipfs/QmSJ2V1yA7FrSCzSfMKw8FMNhwv8W2QzAZLxV5ScYKZDUv\",\"external_url\":\"https://staging.realitems.io/items/Q6Xr6X9Z\",\"component\":\"shopify\",\"productId\":1,\"name\":\"BISOU BOTANICALS\",\"description\":\"Afternoon Delight is a seductively spicy herbal chai with heart-healthy hibiscus, adaptogens  + 20 mg CBD per serving, formulated to promote a healthy libido and sensual relaxation.\",\"attributes\":[{\"value\":\"tea\",\"trait_type\":\"ProductType\"},{\"value\":\"https://www.youtube.com/embed/ab7yGLSJhWs\",\"trait_type\":\"Video\"},{\"value\":\"https://www.theteaspot.com/pages/b-corp-certified-tea\",\"trait_type\":\"RecyclingManual\"},{\"value\":\"\",\"trait_type\":\"MadeIn\"},{\"trait_type\":\"Warning \"},{\"value\":\"Afternoon Delight\",\"trait_type\":\"ProductName\"},{\"value\":\"\",\"trait_type\":\"Music\"},{\"value\":[\"Hibiscus\",\"Rooibos\",\"Peppercorn\",\"Cinnamon\",\"Lemongrass\",\"Ginger\",\"Cardamom Seeds\",\"CBD\"],\"trait_type\":\"FeaturesArray\"},{\"value\":\"Our fanciful, flavorful teas harness the synergy of pure CBD with organic adaptogens to bring you products that you will both trust and love!  This stellar collection represents our collective knowledge and passion from 32 years in the tea industry.\",\"trait_type\":\"SecretMessage\"},{\"value\":\"National Race to End Women's Cancer\",\"trait_type\":\"CharityDonationRecipient\"},{\"value\":\"\",\"trait_type\":\"CharityDonationAmount\"},{\"value\":\"We believe that tea every day is vital for wellness and self-care, and strive to enlighten and enliven those who consume it. In fact, we’re proponents of drinking 5 cups a day, to continually support our immune systems on a cellular level, as our founder advocates in her book Cancer Hates Tea.\",\"trait_type\":\"CharityMessage\"},{\"value\":\"\",\"trait_type\":\"NotifyThirdParty\"},{\"value\":\"https://realitems.org/ipfs/QmP14Egsho7BUXVCtPszP43GFJ7hx65TCvnrN78WtjPpCV\",\"trait_type\":\"IPFSBrandLogo\"},{\"value\":\"https://realitems.org/ipfs/QmfPGKLcTGgQC9LDBubVtfUM29i2tLJYhaAPmSiHpwHVvg\",\"trait_type\":\"IPFSCertification\"},{\"value\":\"https://realitems.org/ipfs/QmSJ2V1yA7FrSCzSfMKw8FMNhwv8W2QzAZLxV5ScYKZDUv\",\"trait_type\":\"IPFSproductPhoto1\"},{\"value\":\"https://realitems.org/ipfs/QmNU5H3u5LyqkCQzWLHUYqHeTNWqheHURFm6gHXoCGv4QV\",\"trait_type\":\"IPFSproductPhoto2\"},{\"value\":\"https://realitems.org/ipfs/QmfMwgpS5KcRBLZQbuHoTiKE9v4v2GePfPdsWBzQkKBsJP\",\"trait_type\":\"IPFSproductPhoto3\"},{\"value\":\"https://realitems.org/ipfs/QmbMTjpAzqedcqAobC6vDAVGyDLNLULDKbBgr722p4duFQ\",\"trait_type\":\"IPFSproductPhoto4\"},{\"value\":\"https://realitems.org/ipfs/QmUDRF6TuCtqbxTKDeJQoGQQuGArsSnxCX6oLkwekf4Kip\",\"trait_type\":\"IPFSproductPhoto5\"},{\"value\":\"https://realitems.org/ipfs/QmUDMjrYYCQcJJLs1Wkq2Fm71rhLssEtrA5qAFvuGEniLy\",\"trait_type\":\"IPFSproductPhoto6\"},{\"value\":5,\"trait_type\":\"UnitsProduced\"}]}",
                "earmarks": []
            },
            {
                "quantity": 1,
                "tokenUri": "QmbCUHnwcjGejN4RPRTn8vgtrcNjxqP3cUL9Ag5PvEVGxG",
                "timeCreated": "2020-03-26T21:23:21.791838Z",
                "timeModified": "2020-03-26T21:23:21.791838Z",
                "id": 2,
                "obfuscatedId": "JGXA5X8Z",
                "approver": "0xc717b4bc181fabadab58b393116b786238670fc4",
                "productId": 1,
                "externalUrl": "https://staging.realitems.io/items/JGXA5X8Z",
                "stolen": false,
                "notes": "",
                "owned": false,
                "owner": "0x2437d1acb5fe1ed4caea5b45aac26814b1ffd78b",
                "forSale": false,
                "deleted": false,
                "metadata": "{\"image\":\"https://realitems.org/ipfs/QmSJ2V1yA7FrSCzSfMKw8FMNhwv8W2QzAZLxV5ScYKZDUv\",\"external_url\":\"https://staging.realitems.io/items/JGXA5X8Z\",\"component\":\"shopify\",\"productId\":1,\"name\":\"BISOU BOTANICALS\",\"description\":\"Afternoon Delight is a seductively spicy herbal chai with heart-healthy hibiscus, adaptogens  + 20 mg CBD per serving, formulated to promote a healthy libido and sensual relaxation.\",\"attributes\":[{\"value\":\"tea\",\"trait_type\":\"ProductType\"},{\"value\":\"https://www.youtube.com/embed/ab7yGLSJhWs\",\"trait_type\":\"Video\"},{\"value\":\"https://www.theteaspot.com/pages/b-corp-certified-tea\",\"trait_type\":\"RecyclingManual\"},{\"value\":\"\",\"trait_type\":\"MadeIn\"},{\"trait_type\":\"Warning \"},{\"value\":\"Afternoon Delight\",\"trait_type\":\"ProductName\"},{\"value\":\"\",\"trait_type\":\"Music\"},{\"value\":[\"Hibiscus\",\"Rooibos\",\"Peppercorn\",\"Cinnamon\",\"Lemongrass\",\"Ginger\",\"Cardamom Seeds\",\"CBD\"],\"trait_type\":\"FeaturesArray\"},{\"value\":\"Our fanciful, flavorful teas harness the synergy of pure CBD with organic adaptogens to bring you products that you will both trust and love!  This stellar collection represents our collective knowledge and passion from 32 years in the tea industry.\",\"trait_type\":\"SecretMessage\"},{\"value\":\"National Race to End Women's Cancer\",\"trait_type\":\"CharityDonationRecipient\"},{\"value\":\"\",\"trait_type\":\"CharityDonationAmount\"},{\"value\":\"We believe that tea every day is vital for wellness and self-care, and strive to enlighten and enliven those who consume it. In fact, we’re proponents of drinking 5 cups a day, to continually support our immune systems on a cellular level, as our founder advocates in her book Cancer Hates Tea.\",\"trait_type\":\"CharityMessage\"},{\"value\":\"\",\"trait_type\":\"NotifyThirdParty\"},{\"value\":\"https://realitems.org/ipfs/QmP14Egsho7BUXVCtPszP43GFJ7hx65TCvnrN78WtjPpCV\",\"trait_type\":\"IPFSBrandLogo\"},{\"value\":\"https://realitems.org/ipfs/QmfPGKLcTGgQC9LDBubVtfUM29i2tLJYhaAPmSiHpwHVvg\",\"trait_type\":\"IPFSCertification\"},{\"value\":\"https://realitems.org/ipfs/QmSJ2V1yA7FrSCzSfMKw8FMNhwv8W2QzAZLxV5ScYKZDUv\",\"trait_type\":\"IPFSproductPhoto1\"},{\"value\":\"https://realitems.org/ipfs/QmNU5H3u5LyqkCQzWLHUYqHeTNWqheHURFm6gHXoCGv4QV\",\"trait_type\":\"IPFSproductPhoto2\"},{\"value\":\"https://realitems.org/ipfs/QmfMwgpS5KcRBLZQbuHoTiKE9v4v2GePfPdsWBzQkKBsJP\",\"trait_type\":\"IPFSproductPhoto3\"},{\"value\":\"https://realitems.org/ipfs/QmbMTjpAzqedcqAobC6vDAVGyDLNLULDKbBgr722p4duFQ\",\"trait_type\":\"IPFSproductPhoto4\"},{\"value\":\"https://realitems.org/ipfs/QmUDRF6TuCtqbxTKDeJQoGQQuGArsSnxCX6oLkwekf4Kip\",\"trait_type\":\"IPFSproductPhoto5\"},{\"value\":\"https://realitems.org/ipfs/QmUDMjrYYCQcJJLs1Wkq2Fm71rhLssEtrA5qAFvuGEniLy\",\"trait_type\":\"IPFSproductPhoto6\"},{\"value\":5,\"trait_type\":\"UnitsProduced\"}]}",
                "earmarks": [
                    "ken@realitems.io"
                ]
            }
            ....
        }
    }
~~~~


{% include links.html %}
