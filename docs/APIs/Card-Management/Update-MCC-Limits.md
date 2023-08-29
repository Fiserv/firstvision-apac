# Update MCC Limits

This API is used to update the MCC limits to control the card usage. These MCC limits are updated at individual card level.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/mccLimits`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "mccLimitControls": {
    "mccLimitAmount01": "1.00",
    "mccLimitAmount02": "2.00",
    "mccLimitAmount03": "3.00",
    "mccLimitAmount04": "4.00",
    "mccLimitAmount05": "5.00",
    "mccLimitAmount06": "6.00",
    "mccLimitAmount07": "7.00",
    "mccLimitAmount08": "8.00",
    "mccLimitAmount09": "9.00",
    "mccLimitAmount10": "10.00"
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010434272",
  "mccLimitControls": {
    "mccLimitAmount01": "$1.00",
    "mccLimitAmount02": "$2.00",
    "mccLimitAmount03": "$3.00",
    "mccLimitAmount04": "$4.00",
    "mccLimitAmount05": "$5.00",
    "mccLimitAmount06": "$6.00",
    "mccLimitAmount07": "$7.00",
    "mccLimitAmount08": "$8.00",
    "mccLimitAmount09": "$9.00",
    "mccLimitAmount10": "$10.00"
  }
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
    "instance": "/v1/cards/0009846801010434211/mccLimits",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/mccLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0010SF` | Update request - Record not found |
|`V5ED0011SF` | Update request - Record add pending |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
