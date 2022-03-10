# Inquire Statement

 This service is used to fetch statement details for a given account number. 

## Endpoint

`GET /v1/accounts/{accountNumber}/statement/details`

## Payload Example

### Request Payload

```json

Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.***

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/statement/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account. | 



### Successful Response Payload

```json

{
  "personalId": "",
  "fsEndBalance": 0,
  "businessUnit": 600,
  "altDuedelqThreshold": "$0.00",
  "dateLastStatement": "2021-05-07",
  "ytdInterest": "$0.00",
  "daysInCycle": 13,
  "dueDate": "18/09/2021",
  "alternateCustomerNumber": "",
  "accountRelationship": 6000011000000137,
  "interestThisStatement": "$0.00",
  "currentPaymentDue": "$0.00",
  "minimumPayment": 0,
  "cashAvailable": "$0.00",
  "creditLimit": "$150,000.00",
  "storeOrg": 600,
  "projectedDd": "$0.00",
  "ytdLateCharge": "$0.00",
  "statementTransactionDetails": [
    {
      "qualInd": " ",
      "amount": "$1,000.00",
      "cardSequence": 0,
      "merchOrg": 0,
      "authorizationCode": " ",
      "transactionStatus": " ",
      "description": "INITIAL LOAN DISBURSEMENT",
      "cardNbr": 6000011000000137,
      "store": 999999998,
      "dept": " ",
      "transactionCode": 4565,
      "reference": 9.999999980818e+21,
      "transactionType": "D",
      "merchStore": 0,
      "eppConvInd": " ",
      "postDate": "18/08/2021",
      "planSeq": 1,
      "creditPlan": 70001,
      "logicModule": 1,
      "sku": 0,
      "effectiveDate": "18/08/2021",
      "catg": 0
    }
  ],
  "skipPaymentLevel": 0,
  "creditClass": "N1",
  "beginningBalance": "$0.00",
  "currBalanceXchk": "$1,000.00",
  "currentBalance": 0,
  "deferBillBalance": "$0.00",
  "ytdDisclosedCharge": "$0.00",
  "endBalancei": "$0.00",
  "lastYtdInterest": "$0.00",
  "residenceId": 600,
  "debitsNumber": 2,
  "internalStatus": "A",
  "scheduledPaymentAmount": "$0.00",
  "unbilledDebitBalance": "$0.00",
  "billIndicator": 0,
  "billingCycle": 18,
  "noOfQualifiedTxns": 0,
  "unResolvedCreditBalance": "$0.00",
  "shortName": "EPHTIARRAUHROE",
  "numberOfPlans": 1,
  "totalPastDue": "$0.00",
  "statementFlag": "",
  "qualifyingGraceBalance": "$1,500.00",
  "cashLimit": "$3,000.00",
  "creditsAmount": "$0.00",
  "totalPaymentDue": "$0.00",
  "fsAdjustedPoints": 0,
  "dateThisStatement": "18/08/2021",
  "fsEarned": 0,
  "employeeCode": "",
  "fsDisbursedPoints": 0,
  "endBalance": "$1,500.00",
  "fixedPaymentAmount": "$500.00",
  "graceintFree": "$0.00",
  "cycleDue": 0,
  "debitsAmount": "$1,500.00",
  "ytdOverlimitCharge": "$0.00",
  "corresCustomerNumber": " ",
  "amountOfQualifiedTxns": "$0.00",
  "product": 600,
  "creditPlanInterestRateHistory": [
    {
      "lmtNo": " ",
      "creditPlan": 0,
      "periodicInterestRate": "0.0000000%",
      "upToLimit": "$0.00",
      "annualInterestRate": "0.0000000%"
    }
  ],
  "fsBeginningBalance": 0,
  "convertedCreditPlanHistory": [
    {
      "creditPlan": 70001,
      "currentBalance": 0,
      "minimumPayment": 0
    }
  ],
  "creditPlanStatementHistory": [
    {
      "transferrollOut": "$0.00",
      "currentBalance": "$1,500.00",
      "transferrollIn": "$0.00",
      "previousBalance": "$0.00",
      "deferrecapInt": "$0.00",
      "minimumPay": "$0.00",
      "purchasedebits": "$1,5000.00",
      "serviceCharge": "$0.00",
      "periodavgBalance": "$0.00",
      "calculatedYearBase": 1,
      "interest": "$0.00",
      "asChrg": "$0.00",
      "paymentscredits": "$0.00",
      "cycleaverageBalance": "$0.00",
      "creditPlan": 70002,
      "actuarialApr": "0.0000000%",
      "deferInsurance": "$0.00"
    }
  ],
  "graceExpire": "18/09/2021",
  "storeId": 999999998,
  "openToBuy": "$148,000.00",
  "customerNumber": 6000011000000137,
  "recency": 0,
  "relationshipNumber": "",
  "rvlvStatus": "",
  "userCode6": " ",
  "userCode5": " ",
  "userCode4": " ",
  "beginningBalancei": "$0.00",
  "userCode3": " ",
  "totalAmtDueBalance": "$0.00",
  "userCode2": " ",
  "creditsNumber": 0,
  "blockCode1": "",
  "userCode1": " ",
  "billCurrency": "SGD",
  "blockCode2": "",
  "currencyConversionRate": 0,
  "lifeToDateCounter": 1
}
```

### Error Response Payload

```json
{
  "errorCode": "V5S34003SA",
  "errorMessage": "No Statement History information found on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S34003SA` | No Statement History Information Found On File |
| `V5S34003SB` | No Statement History Information Found On File |
| `V5S34003EB` | No Statement History Information Found On File |
| `V5S34003EF` | No Statement History Information Found On File |  
| `V5S34003EG` | No Statement History information found on file |
