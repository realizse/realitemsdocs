---
title: Authentication with the GraphQL API 
keywords: NFT, graphql
sidebar: api_sidebar
permalink: api_authentication.html
tags: [graphql]
folder: api_
---

## We do not proved API Keys.  Instead authentication is handled by OAuth2.

To use the API the client app must first authenticate using a username and password.  Each application connecting to the GraphQL API must have an account (just like a human) in the Real Items system.  To create an account for your application log into the Tokenized Asset Manager, click on Administrators and create an account.

## How it works

Successful authentication will return a JWT token which must be used for the duration of the session.  After authorization, the JWT token must be passed into each request as the Bearer token.  The default session duration for JWT tokens is 24 hours.  The logic for detecting session timeouts and reauthorizing must be coded within the client application.

Here is an example authentication curl request which will return a JWT token.

~~~~
curl --location --request POST 'https://staging.realitems.io/oauth/token' \
--header 'Authorization: Basic cmVhbGl0ZW1zc3RhZ2luZ2NsaWVudGlkOi5CZldjRnk4TUE4KEM=' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'username=joe@realitems.io' \
--data-urlencode 'password=1a/l^k93QGi:'
~~~~

If authentication is successful the response will look something like this.

~~~~
{
    "access_token": "eyJhbGiOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjb3VudHJ5IjoiVVNBIiwidXNlcl9uYW1lIjoia2VuQHJlYWxpdGVtcy5vcmciLCJtb2JpbGUiOiIrNTEwOTMyNDkxMSIsImxhc3RfbmFtZSI6Indvb2RydWZmIiwid2FsbGV0cyI6WyIweGY0ZTVFRjdkZTE1NDQ1QmM1NEU2M0FCMmJGZEM0YkJEY2U0MmUxZkIiLCIweDlFRUNBQjRERjEzQjYzMzhBZDYwMzg4MzVlNjFEQTJENDZjMWRDQjAiXSwiYXV0aG9yaXRpZXMiOlsiU1RBTkRBUkRfVVNFUiIsIkFETUlOX1VTRVIiLCJTVVBFUl9VU0VSIl0sImNsaWVudF9pZCI6InJlYWxpdGVtc3N0YWdpbmdjbGllbnRpZCIsImF1ZCI6WyJyZWFsaXRlbXNzdGFnaW5nand0cmVzb3VyY2VpZCJdLCJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiaWQiOiIyIiwiZXhwIjoxNjE0OTc0Mjg3LCJmaXJzdF9uYW1lIjoia2VuIiwianRpIjoiYTc0MGIyY2YtYWRmOC00MjQ0LWJiMTMtZTdlOGVhODQyZjI1In0.xNuUbl87rN6lCGjuJV5MWpFZR6uG-SYEA4hZv3EFes8",
    "token_type": "bearer",
    "expires_in": 86400,
    "scope": "read write",
    "id": "22",
    "first_name": "joe",
    "last_name": "shmoe",
    "country": "USA",
    "mobile": "+4159324911",
    "wallets": [
        "0xf4e5EF7de15445Bc54E63AB2bFdC4bBDce42e1fB",
        "0x9EECAB4DF13B6338Ad6038835e61DA2D46c1dCB0"
    ],
    "jti": "a740b2cf-adf8-4244-bb13-e7e8ea842f25"
}
~~~~


{% include links.html %}
