# Reset Snooze Count

This API is used to reset the snooze count for a given account's iPlan.

## Endpoint

`PUT /v1/bnpl/{accountId}/resetSnoozeCount`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
}
```

<!--
type: tab
-->

```json
{
    "sequenceNumber": 1,
    "accountId": "0007000022125535509",
    "businessUnit": 700,
    "changeMessage": "SNOOZE COUNT CHANGE IS COMPLETED"
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
        "instance": "/v1/bnpl/0007000022125535501/resetSnoozeCount",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5UI4001SD: ACCOUNT NUMBER NOT FOUND OR IN INVALID STATUS"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/bnpl/{accountId}/resetSnoozeCount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `sequenceNumber` | Query Parameter | *integer* | 5 | This is the iPlan sequence number when each time a new iPlan is created |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5UI4001EA` | Invalid org value in input |
| `V5UI4002EA` | Invalid account number in input |
| `V5UI4003EA` | Invalid rec_nbr in input |
| `V5UI4001SB` | Org in add pending status or not found |
| `V5UI4001SC` | BNPL function not active for the org |
| `V5UI4001SD` | Account number not found or in invalid status |
| `V5UI4001SF` | Error accessing base segment file |
| `V5UI4001SG` | BNPL sequence number is zeros at the account level |
| `V5UI4002SR` | Logo in add pending status or not found |
| `V5UI4001SH` | BNPL function not active for the product |
| `V5UI4002SB` | Installment record is missing for the account |
| `V5UI4002SC` | iPlan activation is still pending |
| `V5UI4002SD` | Snooze function is off at logo level |
| `V5UI4002SE` | Account snooze count is greater than product limit |
| `V5UI4002SG` | Account has payment miss block code |
| `V5UI4002SJ` | Error accessing BNPL offer record |
| `V5UI4002SU` | Error accessing customized account record |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
