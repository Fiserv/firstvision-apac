# Block-Unblock Card

This service is used to update the block codes and the reason codes for the block codes for cards and accounts. Same service can be used to unblock the card by passing spaces in the block-code field of the request body.

## Endpoint

`PUT /v1/cards/{cardNumber}/blockUnblock`

## Payload Example

### Request Payload

```json
{
  "blockCode": "X",
  "warningCode1": "1"
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/blockUnblock).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token number associated with the clear PAN. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "blockCode": "X",
  "blockDate": "19/08/2021",
  "businessUnit": 100,
  "cardNumber": "0009846801010273605",
  "warningCode1": "1"
}

```

### Error Response Payload

```json
{
  "errorCode": "V5ED0301EA",
  "errorMessage": "Priority of new block code cannnot be lower than the existing block code"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED4001SA` | Business unit not found |
| `V5ED4001SB` | Business unit is in Add Pending Status |
| `V5ED4001SC` | Business unit is in Purge Status |
| `V5ED0010SF` | Update Request - Record not found |
| `V5ED0011SF` | Update Request - Record Add Pending |
| `V5ED4002ED` | Card number must be provided |
| `V5ED4003ED` | Card sequence number must be greater than zero |
| `V5ED4004SF` | Invalid Card Sequence |
| `V5ED0301EA` | Priority of new block code cannnot be lower than the existing block code |
| `V5ED0301EB` | Block Code not maintainable for card scheme 0 |
| `V5ED4005ED` | Can't update Block Code when card status is F |  