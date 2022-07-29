# Push Provisioning

This service is used for push provisioning of Visa Card.

## Endpoint

`POST /v1/cards/pushProvisioning`

## Payload Example

### Request Payload

```json
{
  "identifier": "APPLE",
  "version": "1",
  "keysScheme": "FK",
  "ephemeralKey": "",
  "paymentInstrumentId": "0009644806050000069",
  "businessUnit": "100",
  "algorithm": "TDEA",
  "nonce": "123456"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/pushProvisioning).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "addressFields": {
    "addressId": "",
    "addressLine1": "Shinzo abe",
    "addressLine2": "Main",
    "city": "JPN",
    "postalCode": "234226",
    "stateProvince": "Tok"
  },
  "businessUnit": 100,
  "cardholderType": "1",
  "isDynamicCVV2Enabled": "",
  "issueDeliveryOption": "1",
  "paymentInstrumentId": "0009846801010273610",
  "reissueDeliveryOption": "5"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/pushProvisioning",
    "invalid-params": [
      "V5OS4006EB: RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5OS0916SC` | Invalid card number | 
| `V5OS4006EA` | Invalid org | 
| `V5OS4006EB` | Record not found |        

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*