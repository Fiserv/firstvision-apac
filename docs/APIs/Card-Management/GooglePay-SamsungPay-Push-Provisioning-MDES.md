# GooglePay - SamsungPay MDES Push Provisioning

This API is used for push provisioning of MC Card. API validates the incoming card details from client and calls MDES for push multiple accounts. MDES responds with push account recipts which will be further sent to client by FV. 

## Endpoint

`POST /v1/cards/googlePaySamsungPayMDESPushProvisioning`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
XXXXXXX
```

<!--
type: tab
-->

```json
XXXXXXXXXXXXX
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/cards/googlePaySamsungPayPushProvisioning",
    "invalid-params": [
      "V5SG4001SA: INVALID ORG"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/googlePaySamsungPayMDESPushProvisioning).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `requestId` | Payload | *string* | 64 | Unique identifier for the request. |
| `pushAccountId` | Payload | *string* | 36 | Unique identifier for the account that is being pushed. Issuer will need to generate a unique pushAccountId for each funding account/financial account for each request and must pass it in the request. |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `tokenRequestorId` | Payload | *string* | 11 | Identifies the token requestor. |
| `encryptedPayloadExpiryMinutes` | Payload | *string* | 2 | Push Account Request validity period in minutes. This is used to calculate the date/time after which the encrypted payload object will be considered as invalid. MC recommends using a value of 30 minutes. |
| `callBackURL` | Payload | *string* | 256 | Encoded URL for the token requestor to use to pass control back to the Issuer. This needs to be an absolute URL containing the scheme. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5xxxxx` | Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
