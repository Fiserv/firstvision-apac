# Real Time Payments

This service is used post the real-time payments which increases open to buy immediately for a given account number.

## Endpoint

`GET /v1/accounts/realTimePayments`

## Payload Example

### Request Payload

```json
{
  "ticketNumber": 0,
  "letterCode": "",
  "departmentCode": "",
  "salesClerk": "",
  "letterBusinessUnit": 0,
  "referralRepBusinessUnit": 0,
  "accountNumber": "0006000011000000160",
  "referralRepresentativeId": " ",
  "asmRepresentative": "NAB",
  "skuNumber": 0,
  "caseNumber": 5313031301,
  "transactionAmount": 1000,
  "lineData3": "",
  "lineData2": "",
  "referralOption": 0,
  "lineData5": "",
  "cmsBusinessUnit": 600,
  "actionCode": "RLP3",
  "lineData4": "",
  "effectiveDate": "25/02/2022",
  "lineData1": "",
  "asmBusinessUnit": 600,
  "cardNumber": "0006000011000000160"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](..api/?type=get&path=/v1/accounts/realTimePayments).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 3 | Business Unit - Identification number associated with this Account Base Segment record, the values are 001–998 |
| `accountNumber` | Payload | *string* | 19 | Account Number - Unique Identification number of the Account | 
| `actionCode` | Payload | *string* | 4 | Action Code - Action code placed on the account |
| `transactionAmount` | Payload | *number* | 17 | Transaction Amount - Transaction amount to be posted |
 

### Successful Response Payload

```json
{
  "accountBusinessUnit": 600,
  "accountNumber": "0006000011000000160",
  "actionCode": "RLP3",
  "actionCodeDescription": "REAL-TIME PAYMENT3",
  "actionRepId": "NAB",
  "autoReferenceFlag": 1,
  "cardNumber": "0006000011000000160",
  "cashAvailable": "$0.00",
  "clerk": "",
  "creditLimit": "$0.50",
  "currentBalance": "$72.00",
  "departmentCode": "",
  "departmentNumber": "",
  "effectiveDate": "25/02/2022",
  "historyDate": "04/03/2022",
  "historyTime": 144835,
  "letterBusinessUnit": 0,
  "letterCode": "",
  "memoLines": [],
  "name": "RACHEL TEST BY SASHI",
  "openToBuy": "-$166,771.50",
  "referralRepBusinessUnit": 0,
  "referralRepId": "",
  "repBusinessUnit": 600,
  "skuNumber": 0,
  "ticketNumber": "0",
  "transactionAmount": "$10.00",
  "transactionDescription": "API TRANSMISSION TESTING3",
  "workExtension": 0,
  "workPhone": "00000000000000000000"
}
```

### Error Response Payload

```json
{
  "errorCode": "V8MA4005EA",
  "errorMessage": "Account Or Card Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V8MA4005EA` | Account Or Card Not Found |  
| `V8MA4005EB` | Account Or Card Number Required |  
| `V8MA4005EC` | Invalid Account Status |  
| `V8MA4006EB` | ASM Action Code Not On File |  
| `V8MA4006EC` | Action Code Required |    
| `V8MA4013EM` | Transaction Amount Required |  
| `V8MA4013ES` | Transaction Amount Must Be Numeric |  
| `V8MA4001ED` | ASM Not Active  Service Usage Not Allowed |  
| `V8MA4001EF` | Organization Not Found |  
| `V8MA4001ET` | Org Not Found |  
| `V8MA4001SA` | ASM Org Not Found |  
| `V8MA4001EA` | Rep Activity Model Record Not Found On File |  
| `V8MA4002EB` | ASM Rep Invalid Must Be Grater Than Spaces |  
| `V8MA4002EC` | Representative Not Found |  
| `V8MA4002EA` | Rep Tally By Org Model Record Not On File |  
| `V8MA4012EC` | Invalid Effective Date |  
| `V8MA4012EM` | Effective Date Required |  
| `V8MA4016EM` | Dept Is Required |  
| `V8MA4019EM` | SKU Number Required |  
| `V8MA4020EM` | Sales Clerk Required |  
| `V8MA4021EG` | Invalid Letter Code |  
| `V8MA4023EM` | Card Number Required |  
| `V8MA4025EM` | Ticket Number Required |  
| `V8MA4030EG` | Referal Option Must Be Valid 0, Spaces Or 1 |  
| `V8MA4031EG` | Manual Org Must Be Numeric And 001-998 |  
| `V8MA4032EG` | Manual Referal Rep Id Was Not Supplied |  
| `V8MA4036EA` | ASM Rep Not Allowed To Access Account Org |  
