# Activate Card

This service is used to activate the card after successful verification of the cardholder.
>Cardholder verification is the separate API that must be called in the card activation workflow.  Please [click here](./?path=docs/APIs/Card-Management/CVV2-Validation.md) to explore the cardholder verfication APIs.

## Endpoint

`PUT /v1/cards/{cardNumber}/activate`

## Payload Example

### Request Payload

```json
{
  "currentCardRequireActivation": "N",
  "lastCardActivation": "Y"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/activate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "cardSequence": 1,
  "postToAccountNumber": "00010000CCCCC510760",
  "cardNumber": "00098468CCCCC273613",
  "currentCardRequireActivation": "N",
  "cardActivatedDate": "01/10/2021",
  "lastCardActivation": "Y"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4001SA",
  "errorMessage": "Business unit not found in the system"  
}
```

Below table provides the list of application's error code and its description. 

| ErrorCode |  Description |
| --------  | ------------------ |
| `V5ED0010SF` | Update request - record not found |  
| `V5ED0011SF` | Update request - record add pending |
| `V5ED4002ED` | Card number must be provided |
| `V5ED4001SA` | Business unit not found in the system |
| `V5ED4001SB` | Business unit is in add pending status |
| `V5ED4001SC` | Business unit is in purge status |
| `V5ED0309SV` | Invalid current card activation |
| `V5ED0310SV` | Invalid last card activation |