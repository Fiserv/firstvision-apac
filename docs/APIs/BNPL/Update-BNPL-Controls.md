# Update BNPL Controls

This API is used to update BNPL controls at account level for a given account id.

## Endpoint

`PUT /v1/bnpl/{accountId}/bnplControls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000103",
  "configurationTemplate": "BNPLTMPL10",
  "preferredDayOfWeek": 0,
  "bookingAlertChannelIndicator": 0,
  "iplanActivationAlertChannelIndicator": 0,
  "paymentDueAlertChannelIndicator": 0,
  "missedPaymentAlertChannelIndicator": 0,
  "switchAlertChannelIndicator": 0,
  "snoozeAlertChannelIndicator": 0,
  "defaultRepaymentReferenceIndicator": 0
}

```

<!--
type: tab
-->

```json
{
    "businessUnit": 700,
    "accountId": "0007000022102711404",
    "configurationTemplate": "BNPL01TRAN",
    "preferredDayOfWeek": 0,
    "bookingAlertChannelIndicator": 0,
    "iPlanActivationAlertChannelIndicator": 0,
    "paymentDueAlertChannelIndicator": 0,
    "missedPaymentAlertChannelIndicator": 0,
    "switchAlertChannelIndicator": 0,
    "snoozeAlertChannelIndicator": 0,
    "defaultRepaymentReferenceIndicator": 0
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "442201",
        "detail": "Please refer to invalid-params for error details",
        "title": "Unprocessable Entity",
        "instance": "/v1/bnpl/0007000022102711404/bnplControls",
        "source": "VPL",
        "status": 422,
        "invalid-params": [
            "V5BS1304EA: BNPL CONF TEMPLATE IS NOT DEFINED IN THE SYSTEM"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/bnpl/{accountId}/bnplControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
