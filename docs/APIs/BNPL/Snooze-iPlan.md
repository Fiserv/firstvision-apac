# Snooze iPlan

This API is used to snooze the iPlan  for a given account.

## Endpoint

`PUT /v1/bnpl/{accountId}/snoozeIplan`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{}
```

<!--
type: tab
-->

```json
{
  "accountId": "0007000022125535509",
  "sequenceNumber": 2,
  "businessUnit": 700,
  "changeMessage": "UPDATE FUNCTION IS COMPLETED"
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
        "instance": "/v1/bnpl/0007000022090709402/snoozeIplan",
        "source": "VPL",
        "status": 422,
        "invalid-params": [
            "V5UI4004SB: SNOOZE/SWITCH UPDATE IN PROGRESS. IPLAN UPDATE IS NOT ALLOWED"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/bnpl/{accountId}/snoozeIplan).

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
| `V5UI4004SB` | Snooze/switch update in progress. iPlan update is not allowed |
| `V5UI4001SB` | Org in add pending status or not found |
| `V5UI4001SC` | BNPL function not active for the org |
| `V5UI4001SD` | Account number not found or in invalid status |
| `V5UI4001SF` | Error accessing base segment file |
| `V5UI4001SG` | BNPL sequence number is zeros at the account level |
| `V5UI4002SR` | Logo in add pending status or not found |
| `V5UI4001SH` | BNPL function not active for the product |
| `V5UI4002SB` | Installment record is missing for the account |
| `V5UI4002SC` | iPlan activation is still pending  |
| `V5UI4002SD` | Snooze function is off at logo level |
| `V5UI4002SE` | Account snooze count is greater than product limit |
| `V5UI4002SG` | Account has payment miss block code |
| `V5UI4002SH` | All installment is requested. Snooze not allowed |
| `V5UI4002SI` | Snooze not allowed for the offer |
| `V5UI4002SJ` | Error accessing BNPL offer record |
| `V5UI4002SK` | New current instalment date is >= next term instalment date |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
