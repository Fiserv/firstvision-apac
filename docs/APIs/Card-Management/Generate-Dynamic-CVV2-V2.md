# Generate Dynamic CVV2 V2

This API is used to generate encrypted dynamic CVV2 and provide other additional details like encrypted payment card number, encrypted expiry date, embossed name 1, embossed name 2, dynamic CVV2 expire date and time for a given payment instrument Id.

## Endpoint

`POST /v2/cards/generateDynamicCVV2`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 600,
  "paymentInstrumentId": "0009846801010065787",
  "keyAssociation": "NUI"
}
```

<!--
type: tab
-->

```json
{
  "encryptedPaymentCardNumber": "217E8A00536C7A101B055563FBF49C9A",
  "encryptedDynamicCVV2": "C8FB47CB632D1D16",
  "encryptedCardExpiryDate": "6D259F94D6096444",
  "embossedName1": "John Brono ",
  "embossedName2": "Samuel Baro",
  "dynamicCVV2ExpiryDateTime": "27/07/2022 16:00:23"
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v2/cards/generateDynamicCVV2",
    "invalid-params": [
      "V5DC4002SB: ACCT IS PURGED/FRAUD/CLOSED/CGOFF OR ADD PENDING/NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v2/cards/generateDynamicCVV2).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V5DC4002SV/V5DC4002SA` | Card number should be numeric and not zeroes |
| `V5DC4004SV` | Valid values are Y and N for disable DCVV2 method flag |
| `V5DC4003SA` | Key association should be greater than spaces |
| `V5DC4001SA` | Invalid card/org |
| `V5DC4001SB` | Org security failed |  
| `V5DC4002SB` | Acct is purged/fraud/closed/cgoff or add pending/not found |
| `V5DC4002SC` | Acct is billing/control/diversion acct |
| `V5DC4002SD` | Acct warning code is 1/2/3/4/8 |
| `V5DC4002SE` | Card is add pending/purged/fraud/notfnd |
| `V5DC4002SF` | Card warning code is 1/2/3/4/8 |
| `V5DC4002SG` | Card not active |
| `V5DC4002SH` | Card got expired |
| `V5DC4002SJ` | Not valid visa affiliation |
| `V5DC4002SK` | DCVV2 method is static at logo level |
| `V5DC4002SL` | HSM call failed |
| `V5DC4002SM` | DCVV2 method is static at global parm level |
| `V5DC4002SN` | Last generated DCVV2 not expired yet |
| `V5DC4002SO` | Dynamic CVV2 already disabled at card level |
| `V5DC4002SP` | Dynamic CVV2 already enabled at card level |
| `V5DC4002SQ` | Dynamic CVV2 not enabled at card level |
| `V5DC4002SR` | ZEK pan encryption failed |
| `V5DC4002SS` | ZEK DCVV2 encryption failed |
| `V5DC4001IA` | Static CVV2 is set for this card successfully |
| `V5DC4001IB` | Dynamic CVV2 activated and DCVV2 generated successfully |
| `V5DC4003SB` | Key system file not found |
| `V5DC4003SC` | Key system record read fail |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
