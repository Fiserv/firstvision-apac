# Inquire Spend Limits

This API is used to fetch the spending limits to control the card usage. These limits are set to individual card level like maximum ATM, OTC, Retail etc authorization amount and count.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/spendLimits`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Payment Instrument Identification should be sent as path variable..***

<!--
type: tab
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010434272",
  "spendLimitControls": {
    "maximumAtmCashAuthorizationsAmount": "$100.00",
    "maximumAtmCashAuthorizationsCount": 1,
    "maximumAuthorizationsFrequency": "1",
    "maximumOtcAuthorizationsCount": 1,
    "maximumOtcCashAuthorizationsAmount": "$200.00",
    "maximumRetailAuthorizationsAmount": "$100.00",
    "maximumRetailAuthorizationsCount": 1,
    "maximumSingleAtmTransactionAmount": "$100.00",
    "maximumSingleOtcCashAuthorizationAmount": "$100.00",
    "maximumSingleRetailAuthorizationAmount": "$0.00"
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
    "instance": "/v1/cards/0009846801010434271/spendLimits",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0004SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
