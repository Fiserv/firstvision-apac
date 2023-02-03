# GooglePay - SamsungPay VTS Push Provisioning

This service is used for push provisioning of Visa Card when Gpay or Samsung Pay wallet is used. Card push provisioning refers to the creation of a secure digital "copy" of a preexisting card (either physical or virtual). The "copy" is then added to a Gpay or Samsung Pay wallet.

## Endpoint

`POST /v1/cards/googlePaySamsungPayPushProvisioning`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009644706050000069",
  "isIDnV": "true",
  "clientAppID": "myAppID",
  "clientDeviceID": "ed6abb56323ba656521ac476",
  "clientWalletProvider": "40000000047",
  "clientWalletAccountID": "a3-xLSOCatGskD6LRxNuvZG7",
  "alg": "A256GCMKW",
  "enc": "A256GCM",
  "typ": "JOSE",
  "walletProvider": "GOOGLE",
  "intent": "PUSH_PROV_MOBILE"
}
```

<!--
type: tab
--> 

```json
{
  "vtsToken": "eyJraWQiOiJBQkNERUZHSElKS0xNTk9QUVJTVFVWV1hZWkFCQ0RFRkdISUpLTE1OT1BRUlNUVVZXIiwiYWxnIjoiQTI1NkdDTUtXIiwiZW5jIjoiQTI1NkdDTSIsInR5cCI6IkpPU0UiLCJjaGFubmVsU2VjdXJpdHlDb250ZXh0IjoiU0hBUkVEX1NFQ1JFVCIsImlhdCI6IjE2NzQwMjcyMjciLCJpdiI6Il9xTWtpY1Y2MkZKOWhEY3UiLCJ0YWciOiJMRDFOaEQwYy1LcmQwb0ZxRmRSQkpRIn0.RFtrrSb4jr3T857-HqFZX6gW_XKfSEhKcAoGL8Elkjs.YW1GMllYZ3VZM0o1Y0hSdkxuTndaV011U1haUVlYSmhiV1YwWlhKVGNHVmpRRFkyTkRBM1lUTXg.OC3ucDtOFAESzxQ4hznVJdgYISoMqkOCGzm4_Sn4-PP-4uqy2nmvabiSCeUcuVi0bgLdAU2tbwVDX3DojhpampaaCmPkb-uGdluejsOSr5qcMTJTWFTjuuWAa_8vVR2h4IYA1UMRmJPA8jl34RfVkz6TBW1iYOXnBjNnFK-KOJ3NpsurDAJU66yOQ9cxYyUu_aeGb-LsD0QLRzqdBmpLoqZUVl53m0ChoV1OPUxaXzUdFcIXo3B_Znyhn2__Ios0-YPqY9d0y8ht9Etg4tEOYJ-2akhcuxR7Ti7RiKOPqrQgplaL88eRVeA0rQo54E0jz70q-FEBMlea0PABsClKG9YtBvAzjs4mQr8OmB3BlTswJyko_uV33kDDVXkIjA66qE5NU_sKjL2cXMDlFSXWleXKb0gdsAhiY8IHhzZg7Q25l0STXPIZsKU3I-UmoaqH56ne8dawItFwdbSR.CLJntHFT4g5OGKEgzLl6hw"
}
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/googlePaySamsungPayPushProvisioning).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `clientAppID` | Payload | *string* | 32 | Unique identifier for the client application. | 
| `clientDeviceID` | Payload | *string* | 32 | Stable device identification set by Wallet Provider. | 
| `clientWalletProvider` | Payload | *string* | 32 | Client wallet provider is the token requestor’s ID(TRID). |
| `clientWalletAccountID` | Payload | *string* | 32 | Client provided consumer ID that identifies the Wallet account holder entity. | 
| `walletProvider` | Payload | *string* | 32 | Identifies the wallet (Google Pay / Samsung Pay), the payment card is going to be provisioned. |


### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SG4001SA` | RECORD NOT FOUND | 
| `V5SG4001SF` | INVALID ORG | 
| `V5SG4001SA` | CARD NOT FOUND | 
| `V5SG4002SA` | ACCT SHOULD BE NUMRIC AND GREATER THAN ZERO |       

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*