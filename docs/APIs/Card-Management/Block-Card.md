# Block Unblock Card

This API is used to block or unblock the given payment instrument Id.

*While applying block code, system checks the block code priorities defined at the product to decide to either apply the new block code value or retain the existing block code value. No block code priority check will occur when an unblock request is processed through this API.*

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/blockUnblock`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "blockCode": "X",
  "warningCode1": "1"
}
```

<!--
type: tab
-->

```json
{
  "blockCode": "X",
  "blockDate": "19/08/2021",
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010273605",
  "warningCode1": "1"
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
    "instance": "/v1/cards/0009846801010273601/blockUnblock",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/blockUnblock).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED4001SA` | Org not found |
| `V5ED4001SB` | Organization is in add pending status |
| `V5ED4001SC` | BUsiness unit is in purge status |
| `V5ED0010SF` | Update request - Record not found |
| `V5ED0011SF` | Update request - Record Add Pending |
| `V5ED4002ED` | Card number must be provided |
| `V5ED4003ED` | Card sequence number must be greater than zero |
| `V5ED4004SF` | Invalid Card Sequence |
| `V5ED0301EA` | Priority of new block code cannnot be lower than the existing block code |
| `V5ED0301EB` | Block Code not maintainable for card scheme 0 |
| `V5ED4005ED` | Can't update block code when card status is F |  

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
