# Request Authorization 

This service is used for Authorization request on payment instrument id.

## Endpoint

`POST /v1/auth/authRequest`

## Payload Example

### Request Payload

```json
{
  "paymentInstrumentOrCardId": "0009846801010274074",
  "merchantBusinessUnit": 100,
  "merchantId": 999999998,
  "transactionAmount": 1,
  "planId": 10001,
  "expiryDate": 1123,
  "securityCode": 0,
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/authRequest).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `merchantBusinessUnit` | Payload | *string* | 3 | Field that identifies the business unit to which the store is assigned. The values for the business unit are 001–998. |
| `merchantId` | Payload | *string* | 9 | Field that identifies the store identification number. |
| `transactionAmount` | Payload | *number* | 17 | Authorized sales amount in the currency accepted by the particular merchant. |
| `expiryDate` | Payload | *string* | 4 | Valid card expire date should be provided which is of 4 character with MMYY format. |
| `securityCode` | Payload | *string* | 3 | Security code(CVV2/CVC2/CAV2/CVN2) assigned to the payment Instrument id. |

### Successful Response Payload

```json

{
  "accountDetail": {
    "accountBlockCodeDetail": {
      "blockCode1": "",
      "blockCode1Date": "",
      "blockCode2": "",
      "blockCode2Date": ""
    },
    "accountOpenDate": "01/05/2021",
    "accountType": "DEBIT CARD ACCOUNT",
    "cardFeeDate": "00/00/0000",
    "chargeOffReason": "",
    "creditClassficationAndChargeoffStatus": "N1/0",
    "creditLimitOverlimitPercentage:": "$1.00",
    "customerid": "0001000000000150191",
    "dateCgoff": "00/00/0000",
    "delqLstDate": "00/00/0000",
    "delqPymtDays": "000",
    "lastPaymentAmount": "$0.00",
    "lastPaymentDate": "00/00/0000",
    "lastPurchaseAmount": "$0.00",
    "lastPurchaseDate": "00/00/0000",
    "lastReturnCheckDate": "00/00/0000",
    "lastStatementDate": "30/04/2021",
    "returnCheckCount": 0
  },
  "action": "A",
  "authorizationCode": "055290",
  "availableCredit": "$9,059.93",
  "cardBlockCodeAndWarningCode": "/0000000",
  "cashAvailable": "$0.00",
  "collectionDate": "00/00/0000",
  "collectionReason": 0,
  "creditLimit": "$0.00",
  "currentBalance": "$0.00",
  "customerOpenDate": "01/05/2021",
  "customerStatus": "A       ACTIVE",
  "delqDays": 0,
  "disputedAmount": "$0.00",
  "disputedItemCount": 0,
  "expiryDate": "30/04/2024",
  "memoDetail": {
    "memoCreditAmount": "$0.00",
    "memoCreditCount": 0,
    "memoDebitAmount": "$482.07",
    "memoDebitCount": 59
  },
  "paymentDetail": {
    "cycleDue": 0,
    "totalDueAmount": "$0.00"
  },
  "reason": "APPROVED",
  "responseCode": 0,
  "temporaryCreditLimit": "$0.00",
  "transactionAmount": ".01"
}
```

### Error Response Payload

```json
{
  "errorCode": "V7RQ4001SA",
  "errorMessage": "Auth system record not initialized"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V7RQ4001SA` | Auth system record not initialized |
|`V7RQ4001SB` | End-of-day cutoff being processed | 
|`V7RQ4001SC` | After hours update in progress |
|`V7RQ4001EE` | Country code not valid in cms org rec for merch |
|`V7RQ4002EA` | Merch org is required |                                             
|`V7RQ4002EC` | Merch org must be values 001 thru 998 | 
|`V7RQ4003EA` | Merch status invalid for authorizations |
|`V7RQ4003EB` | Merch record blocked for authorizations | 
|`V7RQ4004EB` | Invalid bankcard not found in bin table |                          
|`V7RQ4004EA` | Check digit issue |                                                 
|`V7RQ4006EA` | Amount must be numeric and greater than zero |
|`V7RQ4006EC` | Amount may not contain any decimals | 
|`V7RQ4007EA` | Credit plan nbr is required |
|`V7RQ4007EB` | Credit plan nbr must be values 00001 thru 99998 | 
|`V7RQ4008EA` | Expiration date is invalid |
|`V7RQ4013EC` | Cvv2 presence indicator and cvv2/cvc2/cvn2/cav2 must be entered | 
|`V7RQ4014EC` | Cvv2/cvc2 is entered the presence ind must be 1 |   
