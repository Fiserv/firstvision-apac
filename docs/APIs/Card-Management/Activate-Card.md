# Activate Card

This API is used to activate the card after successful verification of the cardholder for a given payment instrument Id.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/activate`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "currentCardNeedActivation": "N",
  "deactivateOldCard": "Y"
}
```

<!--
type: tab
--> 

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010273613",
  "currentCardNeedActivation": "N",
  "deactivateOldCard": "Y",
  "cardActivatedDate": "03/01/2020"
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
    "instance": "/v1/cards/0009846801010273611/activate",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/activate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes 

Below table provides the list of application's error code and its description. 

| ErrorCode |  Description |
| --------  | ------------------ |
| `V5ED0010SF` | Update request - Record not found |  
| `V5ED0011SF` | Update request - Record add pending |
| `V5ED4002ED` | Card number must be provided |
| `V5ED4001SA` | Org not found in the system |
| `V5ED4001SB` | Organization is in Add pending status |
| `V5ED4001SC` | Business unit is in purge status |
| `V5ED0309SV` | Invalid current card activation |
| `V5ED0310SV` | Invalid last card activation |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*