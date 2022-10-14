# Fetch Clear PAN from Token PAN

This service is used to fetch the encrypted clear pan for the requested First Vision's Token PAN.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/clearPAN`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Payment Instrument Identification should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/clearPAN).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Successful Response Payload

```json
{
  "encryptedPaymentCardNumber": "217E8A00536C7A101B055563FBF49C9A"
}

```
### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/0009846801010273609/clearPAN",
    "invalid-params": [
      "V5C14002SA: Card Number Record Not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5C14009SR` | HSM call For encryption failed |
|`V5C14001SA` | Org record not found |
|`V5C14002SA` | Card number record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*