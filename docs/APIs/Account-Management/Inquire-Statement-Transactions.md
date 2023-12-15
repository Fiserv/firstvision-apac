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
  "shortName": "EPHTIARRAUHROE",
  "billingCycle": 18,
  "residenceId": "600",
  "customerId": "0002000000050256486",
  "accountStatus": "A",
  "statementModeOrStatus": "",
  "lifeToDateCount": 1,
  "alternateCustomerId": "",
  "creditClass": "N1",
  "blockCode1": "",
  "blockCode2": "",
  "relationshipId": " ",
  "employeeCode": "",
  "dueDetails": {
    "paymentDueDate": "18/09/2021",
    "currentDueAmount": "$0.00",
    "totalPastDueAmount": "$0.00",
    "totalDueAmount": "$0.00"
  },
  "ytdAccumulatorDetails": {
    "interestAmount": "$0.00",
    "lateFeeAmount": "$0.00",
    "overlimitFeeAmount": "$0.00",
    "disclosedFeeAmount": "$0.00",
    "lastInterestAmount": "$0.00"
  },
  "amountDetails": {
    "beginningBalance": "$0.00",
    "qualifiedTransactionsAmount": "$0.00",
    "cashAvailable": "$0.00",
    "cashCreditLimit": "$3,000.00",
    "creditLimit": "$150,000.00",
    "creditsAmount": "$0.00",
    "debitsAmount": "$1,500.00",
    "deferBillBalance": "$0.00",
    "endingBalance": "$1,500.00",
    "fixedPaymentAmount": "$500.00",
    "graceInterestFree": "$0.00",
    "thisStatementInterestAmount": "$0.00",
    "openToBuy": "$148,000.00",
    "projectedDdAmount": "$0.00",
    "qualifyingGraceBalance": "$1,500.00",
    "scheduledPaymentAmount": "$0.00",
    "calculatedInstallmentAmount": "$0.00",
    "unResolvedCreditBalance": "$0.00",
    "unbilledDebitBalance": "$0.00",
    "currentBalanceCrossCheck": "$1,000.00",
    "addOnAmount": "$0.00",
    "overLimitAmount": "$0.00"
  },
  "transactionDetails": [
    {
      "eppConversionIndicator": " ",
      "merchantStore": 0,
      "qualifyingIndicator": " ",
      "category": 0,
      "department": " ",
      "skuNumber": 0,
      "merchantBusinessUnit": 0,
      "paymentInstrumentId": "0002000010000066752",
      "transactionStatus": " ",
      "authorizationCode": " ",
      "description": "INITIAL LOAN DISBURSEMENT",
      "referenceNumber": "09999999980818000060018",
      "planId": 70001,
      "transactionCode": 4565,
      "transactionType": "D",
      "amount": "$1,000.00",
      "postingDate": "18/08/2021",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 50367,
      "merchantCity": "Delhi",
      "maskedPaymentCardNumber": "000484680XXXXXX9405",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 1,
      "merchantCountryCode": "AUS",
      "billerCode": " "
    }
  ],
  "correspondingCustomerId": " ",
  "debitCount": 2,
  "creditCount": 0,
  "cycleDue": 0,
  "dateFieldsDetails": {
    "thisStatementDate": "18/08/2021",
    "lastStatementDate": "05/08/2021",
    "graceExpiryDate": "18/09/2021"
  },
  "daysInCycle": 13,
  "qualifiedTransactionsCount": 0,
  "personalId": "",
  "billingIndicator": 0,
  "revolvingStatus": "",
  "businessUnit": 200
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
| `V5S34001EA` | Invalid org |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
