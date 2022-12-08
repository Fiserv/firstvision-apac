# Fetch Token PAN from Clear PAN

This service is used to fetch the token pan for the First Vision's clear PAN provided in encrypted format.

## Endpoint

`GET /v1/cards/{encryptedPaymentCardNumber}/tokenPAN`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Encrypted Payment Card Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{encryptedPaymentCardNumber}/tokenPAN).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `encryptedPaymentCardNumber` | Path Variable | *string* | 32 | Unique identification number that appears on the front of the card (PAN) in encrypted format. |

### Successful Response Payload

```json
{
  "paymentInstrumentId": "0009544410000000047"
}
```
### Error Response Payload

```json
[
    {
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/cards/217E8A00536C7A101B055563FBF49C9A/tokenPAN",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5CT4002EB: ZEK PAN DECRYPTION FAILED"
        ]
    }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CT4001EA` | Invalid Org number |
|`V5CT4002EA` | Provide valid ZEK encrypted PAN |
|`V5CT4002EB` | ZEK PAN decryption failed |
|`V5CT4002EC` | Token PAN is not found for given encrypted PAN |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
