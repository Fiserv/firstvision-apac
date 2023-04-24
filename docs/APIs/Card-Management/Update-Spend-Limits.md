# Update Spend Limits

This API is used to update the spending limits to control the card usage. These limits are updated at individual card level.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/spendLimits`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "spendLimitControls": {
    "maximumAuthorizationsFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "$10000.00",
    "maximumAtmCashAuthorizationsCount": 1,
    "maximumSingleAtmTransactionAmount": "$10000.00",
    "maximumOtcCashAuthorizationsAmount": "$20000.00",
    "maximumOtcAuthorizationsCount": 1,
    "maximumSingleOtcCashAuthorizationAmount": "$10000.00",
    "maximumRetailAuthorizationsAmount": "$10000.00",
    "maximumRetailAuthorizationsCount": 1,
    "maximumSingleRetailAuthorizationAmount": "$10000.00"
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010434272",
  "spendLimitControls": {
    "maximumAuthorizationsFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "$10000.00",
    "maximumAtmCashAuthorizationsCount": 1,
    "maximumSingleAtmTransactionAmount": "$10000.00",
    "maximumOtcCashAuthorizationsAmount": "$20000.00",
    "maximumOtcAuthorizationsCount": 1,
    "maximumSingleOtcCashAuthorizationAmount": "$10000.00",
    "maximumRetailAuthorizationsAmount": "$10000.00",
    "maximumRetailAuthorizationsCount": 1,
    "maximumSingleRetailAuthorizationAmount": "$10000.00"
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0010SF` | Update request - Record not found |
|`V5ED0011SF` | Update request - Record add pending |
|`V5ED0319ED` | ATM cash amt field update is not allowed |
|`V5ED0328EA` | Maximum freq input not allowed when no auth limit overrd |
|`V5ED0320EE` | ATM cash nbr field update is not allowed |
|`V5ED0321EH` | TXN limit atm field update is not allowed |
|`V5ED0322EF` | OTC cash amt field update is not allowed |  
|`V5ED0323EG` | OTC cash nbr field update is not allowed |
|`V5ED0324EI` | Txn limit otc field update is not allowed |
|`V5ED0325EB` | Retail amt field update is not allowed |
|`V5ED0326EC` | Retail nbr field update is not allowed |
|`V5ED0327EJ` | Txn limit retail field update is not allowed |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
