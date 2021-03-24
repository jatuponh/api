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

```json
curl -H 'Accept: application/json' -H "key: ${API KEY}" -X GET https://api.hubspace.co.th/${PATH}
```