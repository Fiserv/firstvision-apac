# Validate CVV2

This API is used to validate the CVV2 for a given payment instrument Id along with expiry date.

## Endpoint

`POST /v1/cards/validateCVV2`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010065787",
  "CVV2": "855",
  "expiryDate": "1123"
}

```

<!--
type: tab
--> 

```json
{
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
    "instance": "/v1/cards/validateCVV2",
    "invalid-params": [
      "V5VC4003AE: Invalid CVV2"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/validateCVV2).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `cvv2` | Payload | *string* | 3 | CVV2 value of the card |
| `expiryDate` | Payload | *date* | 4 | Field that indicates the card expiry date in MMYY format | 

### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5VC4001EA` | Invalid org number |
|`V5VC0287EA` | Org not found or in add-pending status |
|`V5VC4002EA` | Invalid card number |
|`V5VC4002EA` | Card number not found |
|`V5VC4004AE` | Invalid expiry date |
|`V5VC4003AE` | Invalid CVV2 | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
