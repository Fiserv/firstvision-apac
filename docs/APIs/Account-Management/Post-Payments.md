# Post Payments

This service is used post the real-time payments which increases open to buy immediately for a given account number without waiting for nightly processing takes place.

## Endpoint

`POST /v1/accounts/postPayments`

## Payload Example

### Request Payload

```json
{
  "businessUnit": "600",
  "accountId": "0006000011000000160",
  "actionCode": "RLP3",
  "transactionAmount": "1000.0",
  "effectiveDate": "25/02/2022",
  "departmentCode": "",
  "skuNumber": 0,
  "salesClerk": "",
  "paymentInstrumentId": "0000000000000000000",
  "ticketNumber": "0",
  "caseNumber": "05313031301",
  "actionNotes": {
    "note1": "",
    "note2": "",
    "note3": "",
    "note4": "",
    "note5": ""
  },
  "representativeDetails": {
    "representativeId": "NAB",
    "referralOption": "0",
    "referralRepBusinessUnit": 0,
    "referralRepresentativeId": " "
  },
  "letterDetails": {
    "letterCode": "",
    "letterBusinessUnit": "0"
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/postPayments).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `actionCode` | Payload | *string* | 4 | Action code placed on the account. | 
| `transactionAmount` | Payload | *number* | 17 | Transaction amount to be posted. |

### Successful Response Payload

```json

{
  "accountBusinessUnit": 600,
  "accountId": "0006000011000000160",
  "actionCode": "RLP3",
  "actionCodeDescription": "REAL-TIME PAYMENT3",
  "actionNotes": {
    "note1": "",
    "note2": "",
    "note3": "",
    "note4": "",
    "note5": ""
  },
  "actionRepId": "NAB",
  "autoReferenceFlag": "1",
  "balances": {
    "cashAvailable": "$0.00",
    "creditLimit": "$0.50",
    "currentBalance": "$72.00",
    "openToBuy": "-$166,771.50"
  },
  "clerk": "",
  "departmentCode": "",
  "effectiveDate": "25/02/2022",
  "historyDate": "29/06/2022",
  "historyTime": 75047,
  "letterDetails": {
    "letterBusinessUnit": 0,
    "letterCode": ""
  },
  "name": "RACHEL TEST BY SASHI",
  "paymentInstrumentId": "0006000011000000160",
  "representativeDetails": {
    "referralRepBusinessUnit": 0,
    "referralRepId": "",
    "repBusinessUnit": 600
  },
  "skuNumber": 0,
  "ticketNumber": "0",
  "transactionAmount": "$100.00",
  "transactionDescription": "API TRANSMISSION TESTING3",
  "workExtension": 0,
  "workPhone": "00000000000000000000"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/postPayments",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get Request - Record not found |  
| `V8MA4005EA` | Account or card not found |  
| `V8MA4005EB` | Account or card number required |  
| `V8MA4005EC` | Invalid account status |  
| `V8MA4006EB` | ASM action code not on file |  
| `V8MA4006EC` | Action code required |    
| `V8MA4013EM` | Transaction amount required |  
| `V8MA4013ES` | Transaction amount must be numeric |  
| `V8MA4001ED` | ASM not active  service usage not allowed |  
| `V8MA4001EF` | Organization not found |  
| `V8MA4001ET` | Org not found |  
| `V8MA4001SA` | ASM org not found |  
| `V8MA4001EA` | Rep activity model record not found on file |  
| `V8MA4002EB` | ASM rep invalid must be grater than spaces |  
| `V8MA4002EC` | Representative Not Found |  
| `V8MA4002EA` | Rep tally by org model record not on file |  
| `V8MA4012EC` | Invalid effective date |  
| `V8MA4012EM` | Effective date required |  
| `V8MA4016EM` | Dept is required |  
| `V8MA4019EM` | SKU number required |  
| `V8MA4020EM` | Sales clerk required |  
| `V8MA4021EG` | Invalid letter code |  
| `V8MA4023EM` | Card number required |  
| `V8MA4025EM` | Ticket number required |  
| `V8MA4030EG` | Referal option must be valid 0, spaces or 1 |  
| `V8MA4031EG` | Manual org must be numeric and 001-998 |  
| `V8MA4032EG` | Manual referal rep ID was not supplied |  
| `V8MA4036EA` | ASM rep not allowed to access account org | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*