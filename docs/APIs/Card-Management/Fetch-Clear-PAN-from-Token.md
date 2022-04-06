# Fetch Clear PAN from Token

This service is used to fetch the clear pan for the requested First Vision's Token PAN.

## Endpoint

`GET /v1/cards/{cardNumber}/clearPan`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Card Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/clearPan).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "cardNumber": 9846801010273604
}
```
### Error Response Payload

```json
{
  "errorCode": "V5CL4002AS",
  "errorMessage": "Token number not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CL4001EA` | Invalid business unit |
|`V5CL4002EA` | Invalid card number |
|`V5CL4001AS` | Business unit not found |
|`V5CL4002AS` | Token number not found |