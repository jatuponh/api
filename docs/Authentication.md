# Authentication

This page describes the authentication methods that you need to implement when making a request to Hub Space API.

We have 2 kinds of authentication methods.

### 1.) Access Token

An ACCESS TOKEN is gotten when you signed in at Hub Space console. The ACCESS TOKEN is mostly used by Hub Space console for creating company, product, coupon, etc.

```json
curl -H 'Accept: application/json' -H "Authorization: Bearer ${ACCESS TOKEN}" -X GET https://api.hubspace.co.th/${PATH}
```

### 2.) API Key

For server-to-server authentication, we use API KEY. API KEY is used for validate coupon, redeem coupon, rollback coupon, etc.

<!-- theme: info -->
> ### How to get an API Key?
> Here is my success callout!
> 1. Go to https://console.hubspace.co.th/setting/authentication.
> 2. Create a new api key by clicking button at the top right corner.
> 3. You will see your new api key as a new record in the table. 

```json
curl -H 'Accept: application/json' -H "key: ${API KEY}" -X GET https://api.hubspace.co.th/${PATH}
```