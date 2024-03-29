# Update Account Charge-Off

This API is used to update account charge-off status.

*User cannot charge off an account with zero balance or credit balance. When performing a manual charge off, the value you enter in the reason field must be defined at the REASON parameter at product level. When the charge-off status of the account is 5 (automatically completed), the value in this field defaults from product level.*

## Endpoint

`PUT /v1/accounts/{accountId}/chargeoff`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "notificationReceivedDate": "01/01/2018",
  "chargeOffReason": "C",
  "chargeOffStatus": "3",
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000509",
  "businessUnit": 600,
  "chargeOffDaysCount": 0,
  "chargeOffReason": "C",
  "chargeOffStatus": "3",
  "notificationReceivedDate": "01/01/2018"
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
    "instance": "/v1/accounts/0006000011000000509/chargeoff",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/chargeoff).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *String* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |
| `V5BS0109SA` | Invalid Internal Status |
| `V5BS0109SB` | PROC Date must be greater than greatest EXP date For purged Acct |
| `V5BS0109SC` | Status cannot change to closed when insurance is Active |
| `V5BS0110EB` | RSN code must be defined |
| `V5BS0110EC` | Cannot Use Chgoff RSN defined In Logo Lvl For Chgoff Sta'2' |
| `V5BS0110SA` | Entered Auto C/O RSN code - CHG To manual Reason |
| `V5BS0110SD` | Cannot use Reason defined for auto chgoff accts |
| `V5BS0110SE` | This charge Off status is not allowed For Edit Or acct has dispute |
| `V5BS0110SF` | Cannot charge Off an account with A zero Or credit balance |
| `V5BS0110SG` | Cannot reset chargeoff On account when days Is > 0 |
| `V5BS0110SH` | Chgoff status update Is not allowed during add |
| `V5BS0184SA` | Not A valid date |
| `V5BS0125SA` | Cannot set A block code On A billing account |
| `V5BS0125SB` | Block code 1 must be alphabetic |
| `V5BS0125SC` | Block code 1 cannot be Replaced With One Of A Lower priority |
| `V5BS0127SA` | Cannot Set A block Code On A Billing account |
| `V5BS0127SB` | Block code 2 must be alphabetic |
| `V5BS0127SC` | Block code cannot be Replaced With One Of A Lower priority |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
