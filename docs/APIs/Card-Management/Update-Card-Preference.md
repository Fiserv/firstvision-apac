# Update Card Preference

This service update fields like cardholder type, issue/reissue delivery options, card address detail and Dynamic CVV2 method for a given payment instrument Id.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/preference`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "cardholderType": "1",
  "reissueDeliveryOption": "5",
  "issueDeliveryOption": "1",
  "isDynamicCVV2Enabled": "0",
  "addressFields": {
    "addressLine1": "Shinzo abe",
    "addressLine2": "Main",
    "city": "JPN",
    "stateProvince": "Tok",
    "postalCode": "234226",
    "addressId": "Home"
  }
}
```

<!--
type: tab
--> 

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
      "V5ED0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/preference).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0010SF` | Update request - record not found | 
| `V5ED0011SF` | Update request - Record add pending | 
| `V5ED0330SV` | Card - invalid  reissue-deliv-option |        
| `V5ED0331SV` | Card - invalid  issue-deliv-option | 
| `V5ED0237SV` | Invalid  cardholder-type |
| `V5ED0237EA` | User not allowed to change cardholder type from 1 to 0 |
| `V5DC4004SV` | Valid values are Y and N for disable Dcvv2 method flag |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*