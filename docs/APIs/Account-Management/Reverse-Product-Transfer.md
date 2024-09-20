# Reverse Product Transfer

This API is used to reverse transfer of the account and all the cards associated to it to a old product.

## Endpoint

`POST /v1/accounts/reverseProductTransfer`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "accountId": "0007000011058359003",
  "businessUnit": 700
}
```

<!--
type: tab
-->

```json
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/reverseProductTransfer",
    "invalid-params": [
      "V5XF4002SA: ACCOUNT NUMBER NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/reverseProductTransfer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5XF4001SB` | No organization record on file |
| `V5XF4002SA` | Account number not found |
| `V5XF4002EM` | Account can not be reversed |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
