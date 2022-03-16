# Inquire Card Controls

This service fetches the card controls for a given card number like maximum number and amount of retail/OTC/Single ATM authorization allowed on card number as well as single otc cash/Retail authorization allowed.

## Endpoint

`GET v1/cards/{cardNumber}/controlDetails`

## Payload Example

### Request Payload

>Should be empty.  
***The Business Unit and Card Number should be sent as query parameters and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/controlDetails).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "maximumAmountOtcCashAuthorizationsAllowed": "$1,000.00",
  "businessUnit": 600,
  "maximumNumberRetailAuthorizationsAllowed": 2,
  "motoFlag": "Y",
  "payWaveSwitch": "N",
  "maximumNumberOtcAuthorizationsAllowed": 5,
  "cashBackTranFlag": "Y",
  "maximumNumberAtmCashAuthorizationsAllowed": 2,
  "singleOtcCashAuthorizationAllowed": "$100.00",
  "maximumAmountSingleAtmTransactionAllowed": "$2,000.00",
  "singleRetailAuthorizationAllowed": "$1,000.00",
  "maximumAmountRetailAuthorizationsAllowed": "$1,000.00",
  "ecomActiveSwitch": 1,
  "atmFlag": "Y",
  "posFlag": "N",
  "maximumAmountAtmCashAuthorizationsAllowed": "$1,000.00",
  "maximumAuthorizationsFrequnecy": 1,
  "intAtmPosFlag": "Y",
  "cardNumber": 9544410000000062
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4003EQ",
  "errorMessage": "Post to acct for dual org not on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EC` | Dual org not found or add pending |
|`V5ED4003EQ` | Post to acct for dual org not on file |