# Inquire Card Controls

This service fetches the card controls for a given card number like maximum number and amount of retail/OTC/Single ATM authorization allowed on card number as well as single otc cash/Retail authorization allowed.

## Endpoint

`GET v1/cards/{cardNumber}/controlDetails`

## Payload Example

### Request Payload

>Should be empty.  
***The Card Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/controlDetails).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "atmFlag": "Y",
  "businessUnit": 100,
  "cardNumber": "0009846801010434751",
  "cashBackTranFlag": "Y",
  "ecomActiveSwitch": "0",
  "intAtmPosFlag": "Y",
  "motoFlag": "Y",
  "payWaveSwitch": "N",
  "posFlag": "N"
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