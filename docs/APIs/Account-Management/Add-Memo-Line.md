# Add Memo Line

The service will validate input message details and add memo line for monetary and non-monetary action applied on account.

## Endpoint

`POST /v1/accounts/addMemoLine`

## Payload Example

### Request Payload

```json
{
  "businessUnit": "600",
  "accountId": "0006000011000000152",
  "actionCode": "AINQ",
  "paymentInstrumentId": " ",
  "actionNotesReq": {
    "note1": "",
    "note2": "",
    "note3": "",
    "note4": "",
    "note5": ""
  }
}

``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/addMemoLine).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `actionCode` | Payload | *string* | 04 | Four character user assigned code for the action.|

### Successful Response Payload

```json
{
  "actionCode": "AINQ",
  "actionCodeDescription": "ACCOUNT INQ",
  "actionNotesRes": {
    "note1": "",
    "note2": "",
    "note3": "",
    "note4": "",
    "note5": ""
  },
  "actionRepId": "NAB",
  "historyDate": "21/05/2022",
  "historyTime": "07:46:44",
  "notePurgeDate": "15/06/2022",
  "notesHistoryStatus": "C",
  "paymentInstrumentId": ""
}

```
### Error Response Payload

```json
{
   errorCode" :  V8NA4004ED" ,
   errorMessage" : Review date must be numeric and greater than zeros"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V8NA4004ED` | Review date must be numeric and greater than zeros |
| `V8NA4003SC` | Action code is required |
| `V8NA4006EG` | Review time is invalid |
| `V8NA4008EI` | Letter org must be numeric and valid values 001-998 |
| `V8NA4010EK` | Card number must be numeric |
| `V8NA4017EA` | Priority must be numeric and valid values are 0 – 3 |
| `V8NA4011EB` | Org-logo can not be determined in validation |
| `V8NA4011SL` | Account is with add pending or to be purged status | 
| `V8NA4071SA` | Embosser record not found |
| `V8NA4016SR` | Action code is not on file |
| `V8NA4020EW` | Review date should be greater than today |
| `V8NA4021EX` | Review date is invalid |
| `V8NA4027EE` | Invalid card number |
| `V8NA4029SA` | Manual referral org/rep not found | 
| `V8NA4030SA` | Manual referral org/rep not eligible for this request |