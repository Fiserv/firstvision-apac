# Inquire Card Preference

This API is used to fetch various details like cardholder type, issue/reissue delivery options, address, Dynamic CVV2 method and address Id etc for a given payment instrument Id.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/preference`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***The Payment Instrument Identification should be sent as path variable.***

<!--
type: tab
--> 

```json
{
  "addressFields": {
    "addressLine1": "Shinzo abe",
    "addressLine2": "Main Tokyo",
    "addressId": "",
    "city": "JPN",
    "postalCode": "234226",
    "stateProvince": "Tok"
  },
  "businessUnit": 100,
  "cardholderType": "1",
  "isDynamicCVV2Enabled": "0",
  "issueDeliveryOption": "1",
  "paymentInstrumentId": "0009846801010273613",
  "reissueDeliveryOption": "5"
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
    "instance": "/v1/cards/0009846801010273611/preference",
    "invalid-params": [
      "V5ED0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/preference).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |


### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V5ED0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
