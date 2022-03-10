# Monetary Action

This service will update the Open-to-Buy, memo debit and credit fields on the Account Base Segment and generate an outstanding authorization record and log records.
  
## Endpoint

`POST /v1/accounts/{accountNumber}/monetaryAction`

## Payload Example

### Request Payload

```json
{
  "ticketNumber": 0,
  "storeNumber": 999999998,
  "flag": " ",
  "authorizationCode": " ",
  "actionCodePriority": 0,
  "departmentCode": " ",
  "salesClerk": " ",
  "letterBusinessUnit": 0,
  "referralRepresentativeId": " ",
  "insuranceCode": " ",
  "skuNumber": 0,
  "referenceNumber": 0,
  "caseNumber": 0,
  "transactionAmount": 3000,
  "lineData3": " ",
  "lineData2": " ",
  "lineData5": " ",
  "actionCode": "AINQ",
  "lineData4": " ",
  "lineData1": " ",
  "walletId": " ",
  "cardSequence": 0,
  "letterCode": " ",
  "referralRepBusinessUnit": 0,
  "foreignUseIndicator": 0,
  "planNumber": 10002,
  "asmRepresentative": "NAB",
  "planSequence": 1,
  "signonName": "string",
  "purchaseOrderNumber": 0,
  "referralOption": 0,
  "securitySignon": "string",
  "effectiveDate": "18/08/2021",
  "asmBusinessUnit": 600,
  "cardNumber": 6000011000000160
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/{accountNumber}/monetaryAction).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `walletID` | Payload | *string* | 3 | This field is the identification Wallet associated with the transaction. |  
| `ticketNumber` | Payload | *string* | 15 | Ticket number (invoice number) associated with the transaction. | 
| `storeNumber` | Payload | *number* | 9 | Store number associated with the transaction. |
| `flag` | Payload | *string* | 3 | flag. | 
| `authorizationCode` | Payload | *string* | 6 | Authorization code associated with the transaction. | 
| `actionCodePriority` | Payload | *number* | 1 | This field helps to set priority for the action code. |  
| `departmentCode` | Payload | *string* | 4 | This field displays the identification of the department code associated with the transaction. | 
| `salesClerk` | Payload | *string* | 12 | Sales clerk associated with the transaction. | 
| `letterBusinessUnit` | Payload | *number* | 3 | This field indicates the business unit of the LTS letter to be sent to the customer. | 
| `referralRepresentativeId` | Payload | *string* | 3 | This field is the identification number of the referral representative. |  
| `insuranceCode` | Payload | *string* | 2 | Code that identifies the insurance product associated with the transaction. | 
| `referenceNumber` | Payload | *string* | 14 | This field is used for the identification of the reference number associated with the transaction. |  
| `caseNumber` | Payload | *number* | 11 | This field is the identification number of the case related to the transaction. |
| `aSMRepresentative` | Payload | *number* | 3 | ASM Representative. | 
| `transactionAmount` | Payload | *number* | 17 | Transaction amount to be posted. | 
| `lineData 1` | Payload | *string* | 60 | This field is used to enter a note for the action to be taken. |  
| `aSMBusinessUnit` | Payload | *string* | 1 | Waive Late Charges. |  
| `lineData2` | Payload | *string* | 60 | This field is used to enter a note for the action to be taken. |  
| `lineData5` | Payload | *string* | 60 | This field is used to enter a note for the action to be taken. | 
| `actionCode` | Payload | *string* | 4 | Action code placed on the account. | 
| `lineData4` | Payload | *string* | 60 | This field is used to enter a note for the action to be taken. |  
| `lineData1` | Payload | *string* | 60 | This field is used to enter a note for the action to be taken. | 
| `sKUNumber` | Payload | *number* | 9 | SKU number associated with the transaction. | 
| `cardSequence` | Payload | *number* | 5 | This field represents the card sequence number associated with the card number of the transaction. | 
| `letterCode` | Payload | *string* | 3 | This field indicates the user-defined letter code of the LTS letter to be sent to the customer through batch processing. | 
| `referralRepBusinessUnit` | Payload | *string* | 3 | This field is the identification number of the Business unit of the referral representative. | 
| `foreignUseIndicator` | Payload | *string* | 1 | Foreign Use Indicator. | 
| `planNumber` | Payload | *number* | 5 | Credit plan number associated with the transaction. |  
| `planSequence` | Payload | *number* | 2 | Sequence number of the plan segment associated with the transaction. |   
| `signonName` | Payload | *number* | 20 | Sign on Name. |  
| `purchaseOrderNumber` | Payload | *string* | 16 | Waive Late Charges. |   
| `referralOption` | Payload | *string* | 1 | This field helps to provide referral option manually. |   
| `securitySignon` | Payload | *string* | 1 | Context name. | 
| `effectiveDate` | Payload | *DATE* | DD/MM/YYYY	 | Date when this action is to take effect. |  
| `cardNumber` | Payload | *string* | 19 | This field represents the card number associated with the transaction. | 


### Successful Response Payload

```json
{
  "insurance": "",
  "storeNumber": 999999998,
  "collectionSequenceNumber": 0,
  "currrencyNod": 2,
  "departmentCode": "",
  "pointsProgram": 0,
  "letterBusinessUnit": 0,
  "transactionDescription": "  ",
  "historyDate": "27/01/2022",
  "notePurgeDate": "00/00/0000",
  "skuNumber": 0,
  "referenceNumber": "",
  "cashAvailable": "$0.00",
  "creditLimit": "$5,000.00",
  "repBusinessUnit": 600,
  "actionCode": "AINQ",
  "resolutionReferenceNumber": 0,
  "cardSequenceNumber": 1,
  "walletId": "",
  "letterCode": "",
  "fundingCardNumber": " ",
  "currentBalance": "$72.00",
  "nextReviewTime": 0,
  "actionRepId": "NAB",
  "transactionCode": 2006,
  "foreignUseIndicator": 0,
  "memoLines": [
    {
      "note": ""
    }
  ],
  "planNumber": 10002,
  "authorizationNumber": "",
  "departmentNumber": "",
  "notesHistoryStatus": "O",
  "name": "RACHEL TEST BY SASHI",
  "cardNumber": 6000011000000160,
  "accountBusinessUnit": 600,
  "ticketNumber": 0,
  "retentionDuration": "",
  "actionCodePriority": 0,
  "workExtension": 0,
  "autoReferenceFlag": 1,
  "nextReviewDate": "00/00/0000",
  "transactionAmount": "$3,000.00",
  "storeBusinessUnit": 0,
  "accountProduct": 1,
  "actionDate": "00/00/0000",
  "actionCodeDescription": "ACCOUNT INQ",
  "declineReason": " ",
  "ctaFile": "",
  "decision": "A",
  "pointsAmount": "$0.00",
  "recordType": "M",
  "planSequenceNumber": 1,
  "referralRepBusinessUnit": 0,
  "openToBuy": "-$80,072.00",
  "accountNumber": 6000011000000160,
  "clerk": "",
  "transactionType": "",
  "feeAmount": "$0.00",
  "purchaseOrderNumber": 0,
  "referralRepId": "",
  "workPhone": 0,
  "historyTime": 101933,
  "currencyCode": 36,
  "effectiveDate": "18/08/2021"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0010SF",
  "errorMessage": "Invalid transaction type"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
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