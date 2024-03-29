# Update Accounts' Address ID

This API is used to update the address ID at account level for a given Account Id upon successful validation of customer ID, if given in the request.

## Endpoint

`PUT /v1/accounts/{accountId}/addressId`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "addressId": "HOME"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": "600",
  "accountId": "0004440010000000017",
  "addressId": "HOME",
  "customerId": "0000000001000000032"
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0004440010000000017/addressId",
    "invalid-params": [
      "V5AU4002SC: ACCOUNT NUMBER NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/addressId).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5AU4002SA` | Account/Card number should not be spaces |
| `V5AU4002SC` | Account number not found |
| `V5AU4002SD` | AMBS record add pending |
| `V5AU4002SF` | AMBS record purged |
| `V5AU4002SG` | AMED record not found |
| `V5AU9910SA` | Address-ID should not be spaces |
| `V5AU0102SA` | Invalid customer number |
| `V5AU4001SF` | Org not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
