# Update Card Type

This service is used to update the type of cardholder between primary and supplementary (Joint Cardholder). 

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/profile`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "cardholderType": "1"
}
```

<!--
type: tab
--> 

```json
{
  "businessUnit": 100,
  "cardholderType": "1",
  "paymentInstrumentId": "0009846801010273613"
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
    "instance": "/v1/cards/0009846801010273612/profile",
    "invalid-params": [
      "V5ED0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/profile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `cardholderType` | Payload | *numeric* | 1 | Pass value 1 for single primary cardholder. Pass value 0 for Joint cardholder. |

### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001SA` | Org not found |
|`V5ED4001SB` | Organization is in add pending status |
|`V5ED4001SC` | Org in purged status |
|`V5ED4001SE` | Invalid org number |
|`V5ED0010SF` | Update request - Record not found |
|`V5ED0011SF` | Update request - Record add pending |
|`V5ED4003ED` | Card sequence must be greater than zeroes |
|`V5ED4004SF` | Invalid card sequence |
|`V5ED0237SV` | Invalid  cardholder-type |
|`V5ED0237EA` | User not allowed to change cardholder type from 1 to 0 |
|`V5ED0237EB` | Cannot have more than one primary card |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
