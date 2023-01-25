# Inquire Statement Transaction Details

This API is used to fetch transaction details and other generic details for a given account Id. Statement date to be provided in input, in order to fetch any specific statement period. If statement date is not given, latest statement details will be fetched.

## Endpoint

`GET /v1/accounts/{accountId}/statementTransactions`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "accountStatus": "A",
  "alternateCustomerId": "",
  "amountDetails": {
    "beginningBalance": "$7.00",
    "calculatedInstallmentAmount": "$0.00",
    "cashAvailable": "$0.00",
    "cashCreditLimit": "$0.00",
    "creditLimit": "$0.00",
    "creditsAmount": "$1,498.68",
    "currentBalance": 0,
    "currentBalanceCrossCheck": "$31.00",
    "debitsAmount": "$1,522.68",
    "deferBillBalance": "$0.00",
    "endingBalance": "$31.00",
    "fixedPaymentAmount": "$0.00",
    "graceInterestFree": "$0.00",
    "openToBuy": "-$31.00",
    "projectedDdAmount": "$0.00",
    "qualifiedTransactionsAmount": "$0.00",
    "qualifyingGraceBalance": "$31.00",
    "scheduledPaymentAmount": "$0.00",
    "thisStatementInterestAmount": "$0.00",
    "unResolvedCreditBalance": "$0.00",
    "unbilledDebitBalance": "$0.00",
    "addOnAmount": "$0.00",
    "overLimitAmount": "$0.00"
  },
  "billingCycle": 8,
  "billingIndicator": 0,
  "blockCode1": "",
  "blockCode2": "",
  "businessUnit": 200,
  "correspondingCustomerId": "",
  "creditClass": "N1",
  "creditCount": 78,
  "currencyConversionRate": 0,
  "customerId": "0002000000050256486",
  "cycleDue": 0,
  "dateFieldsDetails": {
    "graceExpiryDate": "30/06/2021",
    "lastStatementDate": "11/05/2021",
    "thisStatementDate": "30/06/2021"
  },
  "daysInCycle": 0,
  "debitCount": 78,
  "dueDetails": {
    "currentDueAmount": "$0.00",
    "paymentDueDate": "08/07/2021",
    "totalDueAmount": "$0.00",
    "totalDueBalance": "$0.00",
    "totalPastDueAmount": "$0.00"
  },
  "employeeCode": "",
  "lifeToDateCount": 3,
  "minimumPaymentAmount": 0,
  "noOfQualifiedTxns": 0,
  "personalId": "",
  "relationshipId": "",
  "residenceId": "SX1",
  "revolvingStatus": "",
  "shortName": "TEST SHORT NAME",
  "statementModeOrStatus": "",
  "transactionDetails": [
    {
      "amount": "$10.00",
      "authorizationCode": "021447",
      "category": 5999,
      "department": " ",
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "13/05/2021",
      "eppConversionIndicator": " ",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "merchantBusinessUnit": "0",
      "merchantStore": 999999998,
      "maskedPaymentCardNumber": "000444001XXXXXX8266",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "13/05/2021",
      "qualifyingIndicator": "3",
      "referenceNumber": "VT211330002000010000025",
      "skuNumber": 0,
      "transactionCode": 4000,
      "transactionStatus": " ",
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345674"
    },
    {
      "amount": "$1.00",
      "authorizationCode": "021447",
      "category": 5999,
      "department": " ",
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "13/05/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "eppConversionIndicator": " ",
      "merchantBusinessUnit": "0",
      "merchantStore": 999999998,
      "maskedPaymentCardNumber": "000444001XXXXXX5412",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "13/05/2021",
      "qualifyingIndicator": "3",
      "referenceNumber": "VT211330002000010000026",
      "skuNumber": 0,
      "transactionCode": 4579,
      "transactionStatus": " ",
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345673"
    },
    {
      "amount": "$10.00",
      "authorizationCode": " ",
      "category": 0,
      "department": " ",
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "13/05/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "eppConversionIndicator": " ",
      "merchantBusinessUnit": "0",
      "merchantStore": 0,
      "maskedPaymentCardNumber": "000444001XXXXXX6752",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "13/05/2021",
      "qualifyingIndicator": " ",
      "referenceNumber": "19999999980513199980010",
      "skuNumber": 0,
      "transactionCode": 7016,
      "transactionStatus": " ",
      "transactionType": "C",
      "uniqueTransactionId": "APP17977700222011344330001112345672"
    },
    {
      "amount": "$5.00",
      "authorizationCode": "027182",
      "category": 6011,
      "department": " ",
      "description": "Westpac ATM              Sydney CBD   AU",
      "effectiveDate": "25/05/2021",
      "eppConversionIndicator": " ",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "merchantBusinessUnit": "200",
      "merchantStore": 999999998,
      "maskedPaymentCardNumber": "000444001XXXXXX5412",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "25/05/2021",
      "qualifyingIndicator": "2",
      "referenceNumber": "ST211450004000010000029",
      "skuNumber": 0,
      "transactionCode": 6701,
      "transactionStatus": " ",
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345671"
    }
  ],
  "ytdAccumulatorDetails": {
    "disclosedFeeAmount": "$0.00",
    "interestAmount": "$0.00",
    "lastInterestAmount": "$0.00",
    "lateFeeAmount": "$0.00",
    "overlimitFeeAmount": "$0.00"
  }
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
    "instance": "/v1/accounts/0002000010000066759/statementTransactions",
    "invalid-params": [
      "V5S34003SD: ACCOUNT NUMBER NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/statementTransactions).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S34003SD` | Account number not found |
| `V5S34003SA/V5S34003SB/V5S34003EB/V5S34003EF/V5S34003EG` | No statement history information found on file |
| `V5S34222EA` | Invalid txn suppresion indicatr valid values are N or Y |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*