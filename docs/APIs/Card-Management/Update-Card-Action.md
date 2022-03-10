# Update Card Action

Card Action on Embosser record enables client to update actions like replacement, reissue, PIN mailer etc. This field (Card Action) determines the action that system performs on that embosser record during the next batch run. 

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.
  
## Endpoint

`PUT /v1/cards/{cardNumber}/action`

## Payload Example

### Request Payload

```json
{
  "cardAction": 1
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/action).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Card Number - Token Number associated with the clear PAN. |
| `cardAction` | Payload | *number* | 1 | Card Action - The card issue action code that determines the action CMS performs during the next run of the Card Issue program. | 

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "cardAction": "1",
  "cardActionDate": "19/08/2021",
  "cardNumber": "0000000001000000115",
  "lastCardAction": 0
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0204EM",
  "errorMessage": "Valid actions are 0 and 1 when a card has never been issued"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0204EC` | Card cannot be reissued |         
| `V5ED0204EE` | Additional card not allowed for smart card |               
| `V5ED0204EM` | Valid actions are 0 and 1 when a card has never been issued |                
| `V5ED0204SV` | AMED - invalid  card-action |         
| `V5ED0222EB` | Value is required and cannot equal spaces |         
