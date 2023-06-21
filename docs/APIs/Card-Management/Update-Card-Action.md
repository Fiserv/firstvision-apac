# Update Card Action

This API is used to update the card action for a given payment instrument Id.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/action`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "cardAction": 1
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "paymentInstrumentId": "0009544410000000021",
  "cardAction": 1,
  "lastCardAction": 1,
  "cardActionDate": " "
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
    "instance": "/v1/cards/0009544410000000022/action",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/action).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0010SF` | Update Request - Record not found |
| `V5ED0204EC` | Card cannot be reissued |
| `V5ED0204EE` | Additional card not allowed for smart card |
| `V5ED0204EM` | Valid actions are 0 and 1 when a card has never been issued |
| `V5ED0204SV` | Invalid  card action |
| `V5ED0222EB` | Value is required and cannot equal spaces |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
