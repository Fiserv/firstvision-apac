# Update Spend Limits 

This service is used to update the spending limits to control the card usage. These limits are set to individual card level like maximum ATM, OTC, Retail etc authorizatoin amount and count.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/spendLimits`

## Payload Example

### Request Payload

```json
{
  "spendLimitControls": {
    "maximumAuthorizationsFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "10000",
    "maximumAtmCashAuthorizationsCount": 1,
    "maximumSingleAtmTransactionAmount": "10000",
    "maximumOtcCashAuthorizationsAmount": "20000",
    "maximumOtcAuthorizationsCount": 1,
    "maximumSingleOtcCashAuthorizationAmount": "10000",
    "maximumRetailAuthorizationsAmount": "10000",
    "maximumRetailAuthorizationsCount": 1,
    "maximumSingleRetailAuthorizationAmount": "0000"
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

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

### Error Response Payload

```json
{
  "errorCode": "V5ED0319ED",
  "errorMessage": "ATM cash AMT field update is not allowed"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0010SF` | Update request - Record not found |
|`V5ED0011SF` | Update request - Record add pending |
|`V5ED4003ED` | Card seq number must be greater than zero |
|`V5ED4004SF` | Invalid card sequence |
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*