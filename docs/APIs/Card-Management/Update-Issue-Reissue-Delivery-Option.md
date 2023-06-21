# Update Issue Reissue Delivery Option

This API is used to update the issue and re-issue delivery options for a given Payment instrument Id.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/issueReissueDeliveryOption`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "issueDeliveryOption": "1",
  "reissueDeliveryOption": "5"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "issueDeliveryOption": "1",
  "paymentInstrumentId": "0009544410000000047",
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
    "instance": "/v1/cards/0009544410000000041/issueReissueDeliveryOption",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/issueReissueDeliveryOption).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0330SV` | Card - invalid  reissue-deliv-option |
| `V5ED0331SV` | Card - invalid  issue-deliv-option |
| `V5ED0010SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
