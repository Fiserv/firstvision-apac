# Update Snooze Count

This API is used to update the snooze count for a given account's iPlan.

## Endpoint

`PUT /v1/bnpl/{accountId}/snoozeCount`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
    "snoozeCount": 2
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000103",
  "sequenceNumber": 2,
  "changeMessage": "SNOOZE FUNCTION IS COMPLETED"
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
        "instance": "/v1/bnpl/0007000022125535509/snoozeCount",
        "source": "VPL",
        "status": 422,
        "invalid-params": [
            "V5UI4002SX: SNOOZE_VAL IS GREATER THAN INSTALMENT SNOOZE COUNT"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/bnpl/{accountId}/snoozeCount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `sequenceNumber` | Query Parameter | *integer* | 5 | This is the iPlan sequence number when each time a new iPlan is created |

*In addition to the above mentioned minimum field, one of the request payload variable is required.

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5UI4001EA` | Invalid org value in input |
| `V5UI4002EA` | Invalid account number in input |
| `V5UI4003EA` | Invalid rec_nbr in input |
| `V5UI4008EA` | Numeric snooze_val is required when snooze_cnt_update_flag is U |
| `V5UI4001SB` | Org in add pending status or not found |
| `V5UI4001SC` | BNPL function not active for the org |
| `V5UI4001SD` | Account number not found or in invalid status |
| `V5UI4001SF` | Error accessing base segment file |
| `V5UI4001SG` | BNPL sequence number is zeros at the account level |
| `V5UI4002SR` | Logo in add pending status or not found |
| `V5UI4001SH` | BNPL function not active for the product |
| `V5UI4002SB` | Installment record is missing for the account |
| `V5UI4002SC` | iPlan activation is still pending |
| `V5UI4002SD` | Snooze fucntion is off at logo level |
| `V5UI4002SE` | Account snooze count is greater than product limit |
| `V5UI4002SG` | Account has payment miss block code |
| `V5UI4002SJ` | Error accessing BNPL offer record |
| `V5UI4002SU` | Error accessing customized account record |
| `V5UI4002SX` | Snooze_val is greater than instalment snooze count |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
