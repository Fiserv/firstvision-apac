# Add Memo Line

This API adds a memo note on customer's account for a non-monetary action code, which can then be viewed by agents servicing the account in the future.

## Endpoint

`POST /v1/accounts/addMemoLine`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000152",
  "actionCode": "AINQ",
  "paymentInstrumentId": " ",
  "actionNotes": {
    "note1": " ",
    "note2": " ",
    "note3": " ",
    "note4": " ",
    "note5": " "
  }
```

<!--
type: tab
-->

```json
{
  "notePurgeDate": "17/09/2022",
  "notesHistoryStatus": "C"
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
    "instance": "/v1/accounts/addMemoLine",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/addMemoLine).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `actionCode` | Payload | *string* | 04 | Four character user assigned code for the action.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |
| `V8NA4001EA/V8NA4001SA` | Organization number not found |
| `V8NA4002EB` | Account or card number required |
| `V8NA4003SC` | Action code is required |
| `V8NA4003SF` | Invalid foreign use indicator |
| `V8NA4004ED` | Review date must be numeric and greater than zeros |
| `V8NA4005SF` | Invalid action type |
| `V8NA4006EG` | Review time is invalid |
| `V8NA4007SA` | Control record not found |
| `V8NA4008EI` | Letter org must be numeric and valid values 001 998 |
| `V8NA4009EJ` | Card sequence must be numeric |
| `V8NA4010EK` | Card numer must be numeric |
| `V8NA4011EB` | Org logo can not be determined in argetol |
| `V8NA4011SF` | Review date not numeric |
| `V8NA4011SL` | Account is with add pending or to be purged status |
| `V8NA4012SF` | Review time not numeric |
| `V8NA4013SO` | Account is not active for dual org |
| `V8NA4014SF` | Invalid org |
| `V8NA4015SQ` | Invalid request on local account |
| `V8NA4016SF` | Card sequence not numeric |
| `V8NA4016SR` | Action code is not on file |
| `V8NA4017EA` | Priority must be numeric and valid values are 0 - 3 |
| `V8NA4017SF` | Invalid action code |
| `V8NA4018EA` | Manual referral option invalid. Must be zero, spaces or 1 |
| `V8NA4018EB` | Manual referral org number must be numeric and < 999 |
| `V8NA4018ET` | No customer service assigned for operator |
| `V8NA4018SF` | Invalid referral option |
| `V8NA4019SF` | Invalid referral org |
| `V8NA4019SU` | Cust service representative no access for appl org |
| `V8NA4020EA` | Manual referral rep id was not supplied |
| `V8NA4020EW` | Review date should be greater than today |
| `V8NA4021EX` | Review date is invalid |
| `V8NA4022EY` | Return mail letter cannot be processed |
| `V8NA4023EA` | Letter application not installed  |
| `V8NA4024SB` | Letter org is not found |
| `V8NA4026ED` | Letter org not found |
| `V8NA4027EE` | Invalid card number |
| `V8NA4028EG` | Card sequence must be numeric or greater than zero |
| `V8NA4029SA` | Manual referral org/rep not found |
| `V8NA4030SA` | Manual referral org/rep not eligible for this request |
| `V8NA4071SA` | Embosser record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
