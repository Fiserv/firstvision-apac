# Add Memo Line

The service will validate input message details and add memo line for monetary and non-monetary action applied on account.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/accounts/addMemoLine`

## Payload Example

### Request Payload

```json
{
  "businessUnit": 600,
  "letterCode": " ",
  "memoLine1": " ",
  "letterBusinessUnit": 0,
  "referralRepBusinessUnit": 0,
  "memoLine5": " ",
  "accountNumber": "0006000011000000152",
  "memoLine4": " ",
  "memoLine3": " ",
  "memoLine2": " ",
  "reviewDate": "31/12/2021",
  "manualReferralOption": 0,
  "referralRepId": " ",
  "actionCode": "AINQ",
  "reviewTime": 0,
  "cardNumber": " "
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/addMemoLine).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Payload | *string* | 19 | Unique identification number of the account.|
| `actionCode` | Payload | *string* | 04 | Four character user assigned code for the action.|

### Successful Response Payload

```json
{
  "Note": [],
  "actionCode": "AINQ",
  "actionCodeDescription": "ACCOUNT INQ",
  "actionRepId": "NAB",
  "authorizationNumber": "",
  "cardNumber": "",
  "cardSequenceNumber": 1,
  "clerk": "",
  "collectionSequenceNumber": "0",
  "ctaFile": "",
  "decision": "",
  "declineReason": "",
  "departmentNumber": "",
  "effectiveDate": "00/00/0000",
  "fundingCardNumber": "",
  "historyDate": "09/03/2022",
  "historyTime": "06:40:23",
  "insurance": "",
  "letterBusinessUnit": 0,
  "letterCode": "",
  "nextReviewDate": "31/12/2021",
  "nextReviewTime": 0,
  "notePurgeDate": "03/04/2022",
  "notesHistoryStatus": "C",
  "planNumber": "0",
  "planSequenceNumber": "0",
  "pointsAmount": "$0.00",
  "pointsProgram": "0",
  "purchaseOrderNumber": "",
  "referenceNumber": "",
  "referralRepBusinessUnit": 0,
  "referralRepId": "",
  "repBusinessUnit": 600,
  "retentionDuration": "",
  "skuNumber": "0",
  "storeBusinessUnit": "0",
  "storeNumber": "0",
  "ticketNumber": "",
  "transactionAmount": "0",
  "transactionType": ""
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