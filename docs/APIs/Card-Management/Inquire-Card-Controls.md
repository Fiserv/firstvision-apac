# Inquire Card Controls

This API is used to fetch the card control restriction flags for a given payment instrument Id and provide details whether the ATM, POS, ECOM etc transitions are enabled or disabled.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/controlDetails`

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
  "businessUnit": 100,
  "isAtmEnabled": "Y",
  "isCashBackEnabled": "Y",
  "isEcomEnabled": 0,
  "isInternationalAtmPosEnabled": "Y",
  "isMotoEnabled": "Y",
  "isPayWaveEnabled": "N",
  "isPosEnabled": "N",
  "paymentInstrumentId": "0009846801010434751"
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
    "instance": "/v1/cards/0009846801010434752/controlDetails",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/controlDetails).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
