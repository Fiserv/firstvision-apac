# Inquire Card Spend Statistics

This API is used to fetch the spending limit statistics to control the card usage. These limits are set at individual card level.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/spendStatistics`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Payment Instrument Identification should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "atmCashAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  },
  "businessUnit": 600,
  "otcCashAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  },
  "paymentInstrumentId": "0009544410000000047",
  "retailAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  }
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
    "instance": "/v1/cards/0009544410000000047/spendStatistics",
    "invalid-params": [
      "V5ED0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/spendStatistics).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

## Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EL` | Get Request - Record not found |
|`V5ED4001EN` | Record purged or add pending |
|`V5ED4002EA` | Invalid card nmber |
|`V5ED4002ED` | Card number must be provided |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
