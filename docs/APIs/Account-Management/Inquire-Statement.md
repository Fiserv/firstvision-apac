# Inquire Statement

This service is used to fetch statement details for a given account number.

## Endpoint

`GET /v1/accounts/{accountNumber}/statementDetails`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/statementDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique identification number of the account. | 

### Successful Response Payload

```json

{
  "accountRelationship": "0006000011000000137",
  "altDuedelqThreshold": "$0.00",
  "alternateCustomerNumber": "",
  "amountOfQualifiedTxns": "$0.00",
  "appInterestAmount": "$0.00",
  "beginningBalance": "$0.00",
  "beginningBalancei": "$0.00",
  "billCurrency": "",
  "billIndicator": 0,
  "billingCycle": 18,
  "blockCode1": "",
  "blockCode2": "",
  "businessUnit": 600,
  "calculatedInterestAmount": "$0.00",
  "cashAvailable": "$3,930.00",
  "cashLimit": "$4,000.00",
  "convertedCreditPlansRes": {
    "conversionHistoryRes": []
  },
  "corresCustomerNumber": "",
  "creditClass": "N1",
  "creditLimit": "$4,000.00",
  "creditPlanInterestRes": {
    "rateHistoryRes": []
  },
  "creditPlansRes": {
    "historyRes": [
      {
        "actuarialApr": "0.1250000%",
        "asChrg": "$0.00",
        "calculatedYearBase": 1,
        "creditPlan": "10002",
        "currentBalance": "$70.00",
        "cycleaverageBalance": "$8.46",
        "deferInsurance": "$0.00",
        "deferrecapInt": "$0.04",
        "interest": "$0.00",
        "minimumPay": "$0.00",
        "paymentscredits": "$0.00",
        "periodavgBalance": "$8.46",
        "previousBalance": "$0.00",
        "purchasedebits": "$70.00",
        "serviceCharge": "$0.00",
        "transferrollIn": "$0.00",
        "transferrollOut": "$0.00"
      }
    ]
  },
  "creditsAmount": "$0.00",
  "creditsNumber": 0,
  "currBalanceXchk": "$70.00",
  "currencyConversionRate": 0,
  "currentBalance": 0,
  "currentPaymentDue": "$0.00",
  "customerNumber": "9006000000000300031",
  "cycleDue": 0,
  "dateLastStatement": "05/08/2021",
  "dateThisStatement": "18/08/2021",
  "daysInCycle": 13,
  "debitsAmount": "$70.00",
  "debitsNumber": 3,
  "deferBillBalance": "$0.00",
  "dueDate": "02/09/2021",
  "employeeCode": "",
  "endBalance": "$70.00",
  "endBalancei": "$0.00",
  "fixedPaymentAmount": "$0.00",
  "fsAdjustedPoints": "0",
  "fsBeginningBalance": "0",
  "fsDisbursedPoints": "0",
  "fsEarned": "0",
  "fsEndBalance": "0",
  "graceExpire": "23/08/2021",
  "graceintFree": "$70.00",
  "interestThisStatement": "$0.00",
  "internalStatus": "A",
  "lastYtdInterest": "$0.00",
  "lifeToDateCounter": 1,
  "minimumPayment": 0,
  "noOfQualifiedTxns": "0",
  "numberOfPlans": 2,
  "openToBuy": "$3,930.00",
  "personalId": "",
  "planNextToken": "6000006000011000000137202123p40001",
  "product": 1,
  "projectedDd": "$0.00",
  "qualifyingGraceBalance": "$70.00",
  "recency": 0,
  "relationshipNumber": "",
  "residenceId": "SX1",
  "rvlvStatus": "",
  "scheduledPaymentAmount": "$0.00",
  "shortName": "",
  "skipPaymentLevel": 0,
  "statementFlag": "",
  "statementTransactionsRes": {
    "detailsRes": [
      {
        "amount": "$12.00",
        "authorizationCode": " ",
        "cardNbr": "0006000011000000137",
        "cardSequence": 1,
        "catg": 0,
        "creditPlan": 10002,
        "dept": " ",
        "description": "DOMESTIC RETAIL PURCHASE",
        "effectiveDate": "16/08/2021",
        "eppConvInd": " ",
        "logicModule": 1,
        "merchOrg": "0",
        "merchStore": 0,
        "planSeq": 1,
        "postDate": "17/08/2021",
        "qualInd": "2",
        "reference": "09999999980816000020016",
        "sku": 0,
        "store": 999999998,
        "transactionCode": 4000,
        "transactionStatus": " ",
        "transactionType": "D"
      },
      {
        "amount": "$8.00",
        "authorizationCode": " ",
        "cardNbr": "0006000011000000137",
        "cardSequence": 1,
        "catg": 0,
        "creditPlan": 10002,
        "dept": " ",
        "description": "DOMESTIC RETAIL PURCHASE",
        "effectiveDate": "16/08/2021",
        "eppConvInd": " ",
        "logicModule": 1,
        "merchOrg": "0",
        "merchStore": 0,
        "planSeq": 1,
        "postDate": "17/08/2021",
        "qualInd": "2",
        "reference": "09999999980816000020024",
        "sku": 0,
        "store": 999999998,
        "transactionCode": 4000,
        "transactionStatus": " ",
        "transactionType": "D"
      },
      {
        "amount": "$50.00",
        "authorizationCode": " ",
        "cardNbr": "0006000011000000137",
        "cardSequence": 1,
        "catg": 0,
        "creditPlan": 10002,
        "dept": " ",
        "description": "MEMBERSHIP FEE ASSESSED",
        "effectiveDate": "18/08/2021",
        "eppConvInd": " ",
        "logicModule": 11,
        "merchOrg": "0",
        "merchStore": 0,
        "planSeq": 1,
        "postDate": "18/08/2021",
        "qualInd": " ",
        "reference": "19999999980818199970110",
        "sku": 0,
        "store": 999999998,
        "transactionCode": 7001,
        "transactionStatus": " ",
        "transactionType": "D"
      }
    ]
  },
  "storeId": 999999998,
  "storeOrg": 600,
  "totalAmtDueBalance": "$0.00",
  "totalPastDue": "$0.00",
  "totalPaymentDue": "$0.00",
  "tranNextToken": "99999999999999999999999999999999999999999999999999999999999999999999999999999999",
  "unResolvedCreditBalance": "$0.00",
  "unbilledDebitBalance": "$0.00",
  "userCode1": "",
  "userCode2": "",
  "userCode3": "",
  "userCode4": "",
  "userCode5": "",
  "userCode6": "",
  "ytdDisclosedCharge": "$0.00",
  "ytdInterest": "$0.00",
  "ytdLateCharge": "$0.00",
  "ytdOverlimitCharge": "$0.00"
}

```

### Error Response Payload

```json
{
  "errorCode": "V5S34003SA",
  "errorMessage": "No statement history information found on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S34003SA/V5S34003SB/V5S34003EB/V5S34003EF/V5S34003EG` | No statement history information found on file |