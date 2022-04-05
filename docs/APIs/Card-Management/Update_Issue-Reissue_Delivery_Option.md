# Issue Reissue Delivery Option

This service is used to update the issue and re-issue delivery options on card.

## Endpoint

`PUT /v1/cards/{cardNumber}/issueReissueDeliveryOption`

## Payload Example

### Request Payload

```json
{
  "issueDeliveryOption": "1",
  "cardReissueDeliveryOption": "5"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/issueReissueDeliveryOption).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "cardNumber": "0009544410000000047",
  "cardReissueDeliveryOption": "5",
  "issueDeliveryOption": "1"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0330SV",
  "errorMessage": "Card - Invalid  Reissue-deliv-option"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0330SV` | Card - Invalid  Reissue-deliv-option |        
| `V5ED0331SV` | Card - Invalid  Issue-deliv-option | 
| `V5ED0010SF` | Update Request - Record not found | 


