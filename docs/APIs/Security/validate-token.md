# Validate Token

This API is used to validate if the given oauth token is valid or not.

## Endpoint

`POST /v1/api/oauth/validateToken`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

XXXXXXXXXXXXXXXXXXXXXXX
```json
{
  "token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImFsbCIsImNsaWVudF9pZCI6IlBPQ19OQUJfRGV2IiwiZmlyc3RWaXNpb25JZCI6IjAwMDAwQVVOQUIiLCJleHAiOjE3NTAzNTc4MDB9.qYzJ5krS5F1shsACN3qcVmpF7zOB8uhE28TvjI37aDAP3ZDMONm0947eRxnWo0AkBdmY6JMDtRH-hYpgEiTg_VrjlkimjeSjdJDEzjLoDgNqVV3bCqY-SuAczan2bJs58L3iXgUWKhj7f9ax9-SUfkFRwX4ELWHrnUA926c4Il-ISoH-g-t-yljLxAzg2Yb9n_8LgYGgvC-1g5ntmzLtpxq6JHCsJM7LCOwhE7tSfeqq9ie5FknUuQuCqFd9wTemDe_-BAzYCVzDLLbq_Ath3HTYoKP-hDRuJAVybizYRQ-YIclAz6OGg9JKrDmZHe3HEOb5U-gKLMf_Mpt4UprW4w"
}

```

<!--
type: tab
-->

```json
{
  "valid": false
}
```

<!--
type: tab
-->

```json
{
xxxxxxxxxxxxxxxxxxxxxx
}
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/api/oauth/validateToken).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `token` | Payload | *string* | 160 | JWT authorization token specific to the environment. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`xxxxxx` | xxxxxxxxxxxxxxxxxxxxxxxxxxxx |  


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*