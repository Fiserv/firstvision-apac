# ApplePay Push Provisioning

This API is used for push provisioning of Visa Card. Card push provisioning refers to the creation of a secure digital copy of a pre-existing card (either physical or virtual). The "copy" is then added to a Apple Pay wallet.


## Endpoint

`POST /v1/cards/applePayPushProvisioning`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

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

<!--
type: tab
--> 

```json
{
  "provisionActivation": "MBPAC-1-FK-APPLE-  -TDEA-B0FAA81964D13652F1887E6ADCDEB2AB9CC237BA183DBAC47777692592551A3F57DF1C91E57909D5",
  "provisionAuthantication": "MBPAD-1-FK-APPLE-  -TDEA-59CBFFAE1E77B0DAE976CCABFEDBAD0EB778DC80163E09002DA60AF75FE04BFACD3070EE3FD8C6BCD2DE52D2D69D432B732D73AF95A32002D22C9F6257B7B"
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
    "instance": "/v1/cards/pushProvisioning",
    "invalid-params": [
      "V5OS4005EB: EMBOSSER RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/applePayPushProvisioning).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5OS0916SC` | Invalid card number | 
| `V5OS4006EA` | Invalid org | 
| `V5OS4005EB` | Embosser record not found |        

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*