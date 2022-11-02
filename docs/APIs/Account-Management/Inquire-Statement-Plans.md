# Inquire Statement Plan Details

This service is used to fetch statement credit plan details for a given statement date of cardholder account.

## Endpoint

`GET /v1/accounts/{accountId}/statementPlanDetails`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id and statement date should be sent as path and query parameter.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/statementPlanDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `statementDate` | Query Parameter | *date* | 10 | Period for which the user want to view the statement transaction details of an Account, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control.| 

### Successful Response Payload

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
    "cashCreditLimit": "$3,000.00",
    "cashAvailable": "$0.00",
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
  "correspondingCustomerId": " ",
  "debitCount": 2,
  "creditCount": 0,
  "cycleDue": 0,
  "table3": [
    {
      "planId": 70002,
      "beginningBalance": "$0.00",
      "DebitsAmount": "$1,5000.00",
      "creditsAmount": "$0.00",
      "transferRollInAmount": "$0.00",
      "transferRollOutAmount": "$0.00",
      "interestAmount": "$0.00",
      "serviceFeeAmount": "$0.00",
      "annualPercentageRate": 0,
      "deferInterestAmount": "$0.00",
      "minimumPaymentAmount": "$0.00",
      "deferInsuranceAmount": "$0.00",
      "currentBalance1": "$1,500.00"
    }
  ],
  "dateFieldsDetails": {
    "thisStatementDate": "18/08/2021",
    "lastStatementDate": "05/08/2021",
    "graceExpiryDate": "18/09/2021"
  },
  "dueDetails": {
    "dueDate": "18/09/2021",
    "currentDueAmount": "$0.00",
    "totalPastDueAmount": "$0.00",
    "totalDueAmount": "$0.00",
    "totalDueBalance": "$0.00"
  },
  "daysInCycle": 13,
  "minimumPaymentAmount": 0,
  "noOfQualifiedTxns": 0,
  "personalId": "",
  "currencyConversionRate": 0,
  "billingCurrency": "SGD",
  "billingIndicator": 0,
  "revolvingStatus": "",
  "businessUnit": 200
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0002000010000066750/statementPlanDetails",
    "invalid-params": [
      "V5S34003SD: NO ACCOUNT ON FILE"
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
| `V5S34003SA` | No statement history information found on file |
| `V5S34003SD` | No Account on file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*