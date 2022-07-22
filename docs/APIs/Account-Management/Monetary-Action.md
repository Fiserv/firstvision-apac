# Monetary Action

This service will update the Open-to-Buy, memo debit and credit fields for the given account and generate an outstanding authorization record and log records.
  
## Endpoint

`POST /v1/accounts/monetaryAction`

## Payload Example

### Request Payload

```json

{
  "businessUnit": "600",
  "accountId": "0006000011000000160",
  "actionCode": "AINQ",
  "transactionAmount": "3000.0",
  "effectiveDate": "18/08/2021",
  "departmentCode": " ",
  "skuNumber": 0,
  "salesClerk": " ",
  "paymentInstrumentId": "0006000011000000160",
  "ticketNumber": "0",
  "caseNumber": "0",
  "purchaseOrderNumber": "0",
  "planId": 10002,
  "storeNumber": 999999998,
  "authorizationCode": " ",
  "referenceNumber": "0",
  "actionCodePriority": "0",
  "insuranceCode": " ",
  "actionNotes": {
    "note1": " ",
    "note2": " ",
    "note3": " ",
    "note4": " ",
    "note5": " "
  },
  "representativeDetail": {
    "representativeId": "NAB",
    "referralOption": "0",
    "referralRepBusinessUnit": 0,
    "referralRepresentativeId": " "
  },
  "letterDetail": {
    "letterCode": " ",
    "letterBusinessUnit": "0"
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/monetaryAction).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `actionCode` | Payload | *string* | 4 | Action code placed on the account. | 
| `transactionAmount` | Payload | *number* | 17 | Transaction amount to be posted. |

### Successful Response Payload

```json

{
  "accountId": "0006000011000000160",
  "actionCode": "AINQ",
  "actionCodeDescription": "ACCOUNT INQ",
  "actionDate": "00/00/0000",
  "actionNotes": {
    "note1": "",
    "note2": "",
    "note3": "",
    "note4": "",
    "note5": ""
  },
  "authorizationNumber": "",
  "autoReferenceFlag": 1,
  "businessUnit": 600,
  "cashAvailableAmount": "$0.00",
  "creditLimit": "$0.50",
  "currentBalance": "$72.00",
  "currrencyNod": 2,
  "decision": "A",
  "declineReason": "",
  "departmentCode": "",
  "effectiveDate": "18/08/2021",
  "feeAmount": "$0.00",
  "historyDate": "29/06/2022",
  "historyTime": "73749",
  "insurance": "",
  "letterDetail": {
    "letterBusinessUnit": 0,
    "letterCode": ""
  },
  "name": "RACHEL TEST BY SASHI",
  "nextReviewDate": "00/00/0000",
  "nextReviewTime": 0,
  "notePurgeDate": "00/00/0000",
  "notesHistoryStatus": "O",
  "openToBuy": "-$166,771.50",
  "paymentInstrumentId": "0006000011000000160",
  "planNumber": 10002,
  "pointsAmount": "$0.00",
  "pointsProgram": 0,
  "productId": 1,
  "purchaseOrderNumber": "0",
  "referenceNumber": "",
  "representativeDetail": {
    "actionRepId": "NAB",
    "referralRepBusinessUnit": 0,
    "referralRepId": "",
    "repBusinessUnit": 600
  },
  "resolutionReferenceNumber": "0",
  "retentionDuration": "",
  "salesClerk": "",
  "skuNumber": 0,
  "storeBusinessUnit": 0,
  "storeNumber": 999999998,
  "ticketNumber": "0",
  "transactionAmount": "$300.00",
  "transactionCode": 2006,
  "transactionDescription": "000   000   000   000   000   000   000",
  "transactionType": "",
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
    "instance": "/v1/accounts/monetaryAction",
    "invalid-params": [
      "V5CR0004SF: Get Request - Record not found"
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
| `V5BS0010SF` | Update request - Record not found |
| `V8MA4004EA` | Invalid transaction type | 
| `V8MA4005EA` | Account or card not found | 
| `V8MA4005EB` | Account or card number required | 
| `V8MA4005EC` | Invalid account status | 
| `V8MA4006EA` | Monetary trans file issue in memo post routine | 
| `V8MA4006EB` | Asm action code not on file | 
| `V8MA4006EC` | Action code required | 
| `V8MA4013SQ` | Transaction amount greater than max initial load amount | 
| `V8MA4013EM` | Transaction amount required |
| `V8MA4013SM` | Referral not allowed – overlimit | 
| `V8MA4013ES` | Transaction amount must be numeric | 
| `V8MA4013SR` | Transaction amount greater than max life time load amount | 
| `V8MA4013SP` | Transaction amount less than min initial load amount | 
| `V8MA4001ED` | ASM not active  service usage not allowed | 
| `V8MA4001EF` | Organization not found |
| `V8MA4001ET` | ORG not found | 
| `V8MA4001SA` | ASM org not found | 
| `V8MA4001EA` | Rep activity model record not found on file | 
| `V8MA4002EB` | ASM rep invalid must be grater than spaces |
| `V8MA4002EC` | Representative not found | 
| `V8MA4002EA` | Rep tally by org model record not on file | 
| `V8MA4003ED` | Foreign use indicator invalid must be 0 or 1 | 
| `V8MA4003EE` | Invalid foreign indicator | 
| `V8MA4003EF` | Invalid foreign indicator | 
| `V8MA4012EC` | Invalid effective date | 
| `V8MA4012EM` | Effective date required |
| `V8MA4014EM` | Plan number required | 
| `V8MA4014EN` | Plan number must equal the prepaid plan on acct |
| `V8MA4015EM` | Plan sequence is required |
| `V8MA4016EM` | Dept is required | 
| `V8MA4017EM` | Auth code required | 
| `V8MA4018EM` | Store number required | 
| `V8MA4019EM` | SKU number required | 
| `V8MA4020EM` | Sales clerk required | 
| `V8MA4021EG` | Invalid letter code |  
| `V8MA4023EM` | Card number required | 
| `V8MA4024EM` | Card sequence required |
| `V8MA4025EM` | Ticket number required |
| `V8MA4026EM` | Purchase order number required |
| `V8MA4027EM` | Reference number required |
| `V8MA4028EM` | Insurance product required |
| `V8MA4028EN` | Insurance product not appl for prepaid card |
| `V8MA4029EG` | Priority must be numeric must be 0 to 3 | 
| `V8MA4030EG` | Referal option must be valid 0, spaces or 1 |
| `V8MA4031EG` | Manual org must be numeric and 001-998 | 
| `V8MA4032EG` | Manual referal rep id was not supplied |
| `V8MA4033SB` | Case number must be greater than zero |
| `V8MA4034SA` | Not a valid wallet for load/reload | 
| `V8MA4036EC` | Logo not found |
| `V8MA4036EA` | ASM rep not allowed to access account org | 
| `V8MA4036EN` | Plan not found on file | 
| `V8MA4036EO` | Store number not on file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*