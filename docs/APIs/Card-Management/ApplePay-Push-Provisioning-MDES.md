# ApplePay MDES Push Provisioning

This API is used for push provisioning of Master Card. Card push provisioning refers to the creation of a secure digital copy of a preexisting card (either physical or virtual). The copy is then added to a Apple Pay wallet.

## Endpoint

`POST /v1/cards/applePayPushProvisioningforMDES`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "encryptedDataVersion": "1",
  "nonce": "123456",
  "nonceSignature": "4061d9d63ed",
  "paymentInstrumentId": "0009544410000000047",
  "productType": "DEFAULT_MASTERCARD",
  "tavExpiryMinutes": "05"
}
```

<!--
type: tab
-->

```json
{
  "activationData": {
    "dataValidUntilTimestamp": "2019-07-04T12:09:56.123-07:00",
    "includedFieldsInOrder": "dataValidUntilTimestamp|accountNumber|accountExpiry",
    "keyAlias": "U+002D",
    "signature": "SDleZd6dUnRsceEIquTU2VSFmm7dyldLIgj5DsZl0TT/1wDfr+m6EhKFuXjc0SoX20dkK/UF0bHJ4l3kqdTIWWSTqqAH86HJQ2bWVAN/bIWXVtnvrEHjaLF0XQ+yxiCibg6BjNsh+cjBVNmGPrMP4rlIvJui2LuXyyJYeQVMzP1DrBtEXUNGTYUI6VDrO4EZrJYN7vOleI0P1DsTFd3I3s/E9ei6XwJ6gRJJLva9qtkjgFRCETfYkxOLLGM41u5cfoGeBEUITnKE0fJyz+KKq4EZSVW/41Dfiu+CfcAM71PeBkeD7na6H5pDyNEmZuUqU836DjfbdBtPStYaletO+A==",
    "signatureAlgorithm": "RSA-SHA256",
    "version": "4"
  },
  "encryptedData": {
    "expiration": "04/24",
    "name": "John Appleseed",
    "nonce": "123456",
    "nonceSignature": "4061d9d63ed",
    "primaryAccountNumber": "217E8A00536C7A101B055563FBF49C9A",
    "productType": "DEFAULT_MASTERCARD",
    "version": "1"
  }
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
        "instance": "/v1/cards/applePayPushProvisioningforMDES",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5P24001SB: TOKEN PAN NOT FOUND IN EMOBSSER FILE"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path/v1/cards/applePayPushProvisioningforMDES).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `encryptedDataVersion` | Payload | *string* | 32 | The version number to be used for building encrypted payload. This should be '1' as per ApplePay specifications. |
| `nonce` | Payload | *string* | 32 | A one-time-use nonce provided by Apple.This nonce will be included in the push provisioning payload. |
| `nonceSignature` | Payload | *string* | 162 | A one-time use nonce signed by SE returned as nonceSignature by Apple.This signature will be included in the push provisioning payload. |
| `productType` | Payload | *string* | 162 | The type of card product to be digitized. This is expected to be provided by Apple to Issuer. |
| `tavExpiryMinutes` | Payload | *string* | 2 | Expiry duration in minutes to compute the TAV validity period. |


### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5P24001SA` | Token pan should be numeric |
| `V5P24001SB` | Token pan not found in emobsser file |
| `V5P24001SC` | Product not found |
| `V5P24001SD` | Business unit not found |
| `V5P24001SE` | Zek encryption failed |
| `V5P24006SA` | Encrypteddataversion should be numeric |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
