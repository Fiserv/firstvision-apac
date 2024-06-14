# GooglePay - SamsungPay MDES Push Provisioning

This API is used for push provisioning of Master Card. Card push provisioning refers to the creation of a secure digital copy of a preexisting card (either physical or virtual). The copy is then added to a GooglePay or SamsungPay wallet. 

## Endpoint

`POST /v1/cards/googlePaySamsungPayMDESPushProvisioning`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "callBackURL": "http://www.tokenIssuer1.com/pushtoken",
  "encryptedPayloadExpiryMinutes": "30",
  "isAccountHolderDataSupplyEnabled": false,
  "isCompleteIssuerAppActivationEnabled": true,
  "isCompleteWebsiteActivationEnabled": true,
  "isIssuerInitiatedDigitizationDataEnabled": false,
  "locale": "en_US",
  "paymentInstrumentId": "0009544410000000047",
  "pushAccountId": "CA-132d72d4fcb2f4136a0532d3093ff1ab",
  "pushAccountReceiptsValidityPeriod": 15,
  "requestId": "123456",
  "tokenRequestorId": "50123456789"
}
```

<!--
type: tab
-->

```json
{
  "responseId": "123456",
  "pushAccountReceipts": [
    {
      "pushAccountId": "CA-132d72d4fcb2f4136a0532d3093ff1ab",
      "pushAccountReceipt": "MCC-C307F0AE-298E-48EB-AA43-A7C40B32DDDE",
      "issuerInitiatedDigitizationData": "eyJmdW5kaW5nQWNjb3VudEluZm8iOnsicHVzaEFjY291bnRSZWNlaXB0IjoiTUNDLVNUTC00OTZCNjNBOC02OTQzLTRFM0YtOEYzNi1DMjU0M0Q4OTg1ODQifX0="
    }
  ],
  "availablePushMethods": [
    {
      "type": "WEB",
      "uri": "http://www.tokenrequestor1.com/pushtoken"
    }
  ],
  "signature": "ew0KImFsZyI6ICJSUzI1NiIsDQoNCiJraWQiOiAiYXNkZmctcXdlcnR5LXp4Y3ZiIg0KfQ.ew0KDQrCoCJwdXNoQWNjb3VudFJlY2VpcHQiOiAiTUNDLVNUTC0xMzQzMTNCRi01NTg1LTRFNzEtQUIyNC1FQ0RCQzI4RjIzRjEiLA0KImlzc3VlckNhbGxCYWNrIjogImh0dHBzOi8vaXNzdWVyY2FsbGJhY2sudXJsIiwNCiJjYWxsYmFja1JlcXVpcmVkIjogdHJ1ZSwNCiJjb21wbGV0ZVdlYnNpdGVBY3RpdmF0aW9uIjogdHJ1ZSwNCiJhY2NvdW50SG9sZGVyRGF0YVN1cHBsaWVkIjogdHJ1ZSwNCiJsb2NhbGUiOiAiZW5fVVMiDQoNCn0.dBjftJeZ4CVP-",
  "tokenRequestorSignatureSupport": true,
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/cards/googlePaySamsungPayMDESPushProvisioning",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5G14003SB: TOKEN PAN NOT FOUND IN EMBOSSER FILE"
        ]
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
| `V5G14003SA` | Token pan should be 19 digits numeric value |
| `V5G14003SB` | Token pan not found in embosser file |
| `V5G14003SC` | Product not found |
| `V5G14003SD` | Business unit not found |
| `V5G14004SA` | Token requestor id should be 11 digit numeric value |
| `V5G14005SA` | Business unit not found |
| `V5G14005SA` | Encryptedpayloadexpirymins should be 2 digit numeric value |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
