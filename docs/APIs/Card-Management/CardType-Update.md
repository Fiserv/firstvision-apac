# Update Card Type

This service is used to update the type of cardholder between primary and supplementary (Joint Cardholder). 

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/profile`

## Payload Example

### Request Payload

```json
{
  "cardholderType": "1"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/profile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `cardholderType` | Payload | *numeric* | 1 | Pass value 1 for single primary cardholder. Pass value 0 for Joint cardholder. |

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "cardholderType": "1",
  "paymentInstrumentId": "0009846801010273613"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0237SV",
  "errorMessage": "Invalid Cardholder-type"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001SA` | Org not found |
|`V5ED4001SB` | Organization is in Add pending status |
|`V5ED4001SC` | Org in purged status |
|`V5ED4001SE` | Invalid Org Number |
|`V5ED0010SF` | Update Request - Record not found |
|`V5ED0011SF` | Update Request - Record add pending |
|`V5ED4003ED` | Card sequence must be greater than zeroes |
|`V5ED4004SF` | Invalid card sequence |
|`V5ED0237SV` | Invalid  cardholder-type |
|`V5ED0237EA` | User not allowed to change cardholder type from 1 to 0 |
|`V5ED0237EB` | Cannot have more than one primary card |