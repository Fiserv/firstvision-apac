# Update Cards' Address ID

This API is used to update address ID field at card level for given payment instrument Id upon successful validation of customer ID, if given in the request.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/addressId`

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
  "paymentInstrumentId": "0004440010000000017",
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
    "instance": "/v1/cards/0009846801010434752/addressId",
    "invalid-params": [
      "V5AU4002SA: ACCOUNT/CARD NUMBER SHOULD NOT BE SPACES"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/addressId).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `addressId` | Payload | *string* | 15 | Address identifier to determine the type of address. Ex: Home, Office, etc. |

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
| `V5AU9910SB` | Addr-ID should not have spacial chars, only - is allowed |
| `V5AU0102SA` | Invalid customer number |
| `V5AU4001SF` | Org not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
