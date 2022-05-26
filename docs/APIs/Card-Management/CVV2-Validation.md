# CVV2 Validation

The Card Secure Code Validation service is used to validate the CVV2  and optionally the expiry date of a given payment card number. This service is typically called before the card activation or PIN reset service to validate the cardholder.

## Endpoint

`POST /v1/cards/{paymentInstrumentId}/validateCVV2`

## Payload Example

### Request Payload

```json
{
  "cvv2": "855",
  "expiryDate": "1123"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/{paymentInstrumentId}/validateCVV2).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `cvv2` | Payload | *string* | 3 | CVV2 value of the card |
| `expiryDate` | *date* | 10 | Field that indicates the  card expiry date | 

### Successful Response Payload

```json
{
  "paymentInstrumentId": "0009846801010065787"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5VC4003AE",
  "errorMessage": "Invalid CVV2"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5VC4001EA` | Invalid Org Number |
|`V5VC0287EA` | Org not found or in add-pending status |
|`V5VC4002EA` | Invalid card number |
|`V5VC4002EA` | Card number not found |
|`V5VC4004AE` | Invalid expiry date |
|`V5VC4003AE` | Invalid CVV2 | 
