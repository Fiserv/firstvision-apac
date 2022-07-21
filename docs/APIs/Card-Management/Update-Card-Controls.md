# Update Card Controls

This service updates the card controls for a given payment instrument Id like ECOM Active switch, ATM Flag, International ATM POS Flag, MOTO Flag and max Amount ATM/OTC/Retail etc.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/controls`

## Payload Example

### Request Payload

```json
{
  "isPosEnabled": "N",
  "isAtmEnabled": "Y",
  "isPayWaveEnabled": "N",
  "isInternationalAtmPosEnabled": "Y",
  "isCashBackEnabled": "Y",
  "isEcomEnabled": "0",
  "isMotoEnabled": "Y"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/controls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

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
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/0009846801010434752/controls",
    "invalid-params": [
      "V5ED0010SF: Update Request - Record not found"
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
| `V5ED0010SF` | Update request - record not found | 
| `V5ED9555SV` | Invalid pos flag | 
| `V5ED9556SV` | Invalid atm flag |  
| `V5ED8118SV` | Invalid pay wave flag |  
| `V5ED8119SV` | Invalid int atm pos flag |  
| `V5ED8120SV` | Invalid cash back tran flag |  
| `V5ED8117SV` | Invalid ecom act sw |  
| `V5ED9557SV` | Invalid moto flag |  

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*