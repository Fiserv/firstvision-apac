# Update Card Type

This service is used to update the type of cardholder between primary and supplementary (Joint Cardholder). 

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/cards/{cardNumber}/profile`

## Payload Example

### Request Payload

```json
{
    "cardholderType": "1"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/profile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 
| `cardholderType` | Payload | *numeric* | 1 | Pass value 1 for single primary cardholder. Pass value 0 for Joint cardholder |

### Successful Response Payload

```json
{
  "cardholderType": "1",
  "businessUnit": 100,
  "cardSequence": 1,
  "postToAccountNumber": "000100001NNNNN0760",
  "cardNumber": "000984680NNNNN73613"
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
|`V5ED4001SA` | Business unit not found |
|`V5ED4001SB` | Business unit is in Add pending status |
|`V5ED4001SC` | Business unit in purged status |
|`V5ED4001SE` | Invalid business unit |
|`V5ED0010SF` | Update Request - Record not found |
|`V5ED0011SF` | Update Request - Record add pending |
|`V5ED4003ED` | Card sequence must be greater than zeroes |
|`V5ED4004SF` | Invalid card sequence |
|`V5ED0237SV` | Invalid  cardholder-type |
|`V5ED0237EA` | User not allowed to change cardholder type from 1 to 0 |
|`V5ED0237EB` | Cannot have more than one primary card |
