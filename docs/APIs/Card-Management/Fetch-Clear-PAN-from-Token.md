# Fetch Clear PAN from Token

This service is used to fetch the clear pan for the requested First Vision's Token PAN.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/clearPan`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Payment Instrument Identification should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/clearPan).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Successful Response Payload

```json
{
  "paymentCardNumber": "0009846801010273605"
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
|`V5CL4002EA` | Invalid card number |
|`V5CL4001AS` | Org not found |
|`V5CL4002AS` | Token number not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*