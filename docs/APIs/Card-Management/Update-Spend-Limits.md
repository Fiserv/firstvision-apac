# Update Spend Limits 

This service is used to update the spending limits to control the card usage.  These limits are set to individual card level.

## Endpoint

`PUT /v1/cards/{cardNumber}/spendLimits`

## Payload Example

### Request Payload

```json
{
  "spendLimitControlsReq": {
    "maximumAuthorizationsFrequency": "1",
    "maximumAmountAtmCashAuthorizationsAllowed": "10000",
    "maximumNumberAtmCashAuthorizationsAllowed": 1,
    "maximumAmountSingleAtmTransactionAllowed": "10000",
    "maximumAmountOtcCashAuthorizationsAllowed": "20000",
    "maximumNumberOtcAuthorizationsAllowed": 1,
    "singleOtcCashAuthorizationAllowed": "10000",
    "maximumAmountRetailAuthorizationsAllowed": "10000",
    "maximumNumberRetailAuthorizationsAllowed": 1,
    "singleRetailAuthorizationAllowed": "0000"
  }
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "cardNumber": "0009846801010434272",
  "spendLimitControlsRes": {
    "maximumAmountAtmCashAuthorizationsAllowed": "$100.00",
    "maximumAmountOtcCashAuthorizationsAllowed": "$200.00",
    "maximumAmountRetailAuthorizationsAllowed": "$100.00",
    "maximumAmountSingleAtmTransactionAllowed": "$100.00",
    "maximumAuthorizationsFrequency": "1",
    "maximumNumberAtmCashAuthorizationsAllowed": 1,
    "maximumNumberOtcAuthorizationsAllowed": 1,
    "maximumNumberRetailAuthorizationsAllowed": 1,
    "singleOtcCashAuthorizationAllowed": "$100.00",
    "singleRetailAuthorizationAllowed": "$0.00"
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
|`V5ED4001SA` | Business unit not found |
|`V5ED4001SB` | Business unit is in add pending status |
|`V5ED4001SC` | Business unit is in purged status |
|`V5ED4001SE` | Invalid business unit |
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