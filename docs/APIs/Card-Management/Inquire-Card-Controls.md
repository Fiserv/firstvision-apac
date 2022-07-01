# Inquire Card Controls

This service fetches the card controls for a given card like maximum number of transaction count and amount of Retail/OTC/Single ATM authorization, as well as single otc Cash/Retail authorization are allowed on card.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/controlDetails`

## Payload Example

### Request Payload

>Should be empty.  
>
>***The Payment Instrument Identification should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/controlDetails).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "isAtmEnabled": "Y",
  "isCashBackEnabled": "Y",
  "isEcomEnabled": "0",
  "isInternationalAtmPosEnabled": "Y",
  "isMotoEnabled": "Y",
  "isPayWaveEnabled": "N",
  "isPosEnabled": "N",
  "paymentInstrumentId": "0009846801010434751"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0004SF",
  "errorMessage": "Get request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*
