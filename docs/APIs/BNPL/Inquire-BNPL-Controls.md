# Inquire BNPL Controls

This API is used to inquire BNPL controls at account level for a given account id.

## Endpoint

`GET /v1/accounts/{accountId}/bnplControls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
    "businessUnit": 700,
    "accountId": "0007000011253747002",
    "configurationTemplate": "",
    "preferredDayOfWeek": 0,
    "bookingAlertChannelIndicator": 9,
    "iplanActivationAlertChannelIndicator": 9,
    "paymentDueAlertChannelIndicator": 9,
    "missedPaymentAlertChannelIndicator": 9,
    "switchAlertChannelIndicator": 9,
    "snoozeAlertChannelIndicator": 9,
    "defaultRepaymentReferenceIndicator": 0
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/bnpl/0007000011253747001/bnplControls",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5BS0004SF: Get Request - Record not found"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/bnplControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
