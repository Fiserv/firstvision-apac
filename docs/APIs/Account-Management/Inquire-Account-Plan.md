# Inquire Account Plan

This service will retrieve the plan detail as per the account number given in request.

## Endpoint

`GET /v1/accounts/{accountId}/inquirePlan`

## Payload Example

### Request Payload

>Should be empty.
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/inquirePlan).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Successful Response Payload

```json
{
  "accountId": "0002000010000400044",
  "beginningBalance": "$0.00",
  "billedNotPaidDetailsRes": {
    "annualFeeAmount": "$0.00",
    "collectionFeeAmount": "$0.00",
    "insuranceAmount": "$0.00",
    "interestAmount": "$0.00",
    "lateFeeAmount": "$0.00",
    "nsfFeeAmount": "$0.00",
    "overlimitFeeAmount": "$0.00",
    "recoveryFeeAmount": "$0.00",
    "serviceFeeAmount": "$0.00",
    "userFee1Amount": "$0.00",
    "userFee2Amount": "$0.00",
    "userFee3Amount": "$0.00",
    "userFee4Amount": "$0.00",
    "userFee5Amount": "$0.00",
    "userFee6Amount": "$0.00"
  },
  "businessUnit": 200,
  "dateFieldsDetailsRes": {
    "accruedThroughDate": "31/12/2020",
    "billingBeginningDate": "00/00/0000",
    "effectiveDate": "01/03/2021",
    "effectiveRateChangeDate": "00/00/0000",
    "insuranceAssessmentStartDate": "00/00/0000",
    "interestAssessmentStartDate": "00/00/0000",
    "lastPaymentDate": "00/00/0000",
    "paidOutDate": "00/00/0000",
    "paymentBeginningDate": "00/00/0000",
    "paymentTypeIndicatorMaintenanceDate": "00/00/0000",
    "planDate": "01/03/2021",
    "userFee1assessmentDate": "00/00/0000",
    "userFee2assessmentDate": "00/00/0000",
    "userFee3assessmentDate": "00/00/0000"
  },
  "disputedAmount": "$0.00",
  "generalDetailsRes": {
    "consolidatedPayment": "N",
    "consolidatedStatement": "Y",
    "limitIndicator": 0,
    "multipleSales": "Y",
    "planDescription": "",
    "rateType": "",
    "referenceNumber": ""
  },
  "interestTableOverrideDetailsRes": {
    "expiryDate": "00/00/0000",
    "status": "",
    "tableId": 0
  },
  "lastInterestRate": "0.00000%",
  "miscellenousDetailsRes": {
    "balanceTransferMonthsRemaining": 0,
    "cycleToDatePostedPaymentAmount": "$0.00",
    "disclosureDays": 0,
    "fixedPaymentAmount": "$0.00",
    "interestExpiryDisclosureIndicator": "0",
    "lastInterestRateTableUsed": 0,
    "lastPaymentAmount": "$0.00",
    "lastPurchaseBalanceAmount": "$1.00",
    "lastRequestedPaymentAmount": "$0.00",
    "lifeToDateAppliedPaymentAmount": "$0.00",
    "lifeToDateRequestedPaymentAmount": "$0.00",
    "lifeToDateReturnAmount": "$0.00",
    "paymentType": "T",
    "planNumberForConsolidatedPayments": 10002,
    "planStatus": 1,
    "planStatusChangeDate": "00/00/0000",
    "planTotalDueAmount": "$0.00",
    "planType": "R",
    "previousFixedPaymentAmount": "$0.00",
    "previousPlanStatus": 0,
    "rateTableOccurrenceIndicator": 2,
    "userdefinedProductCode": "10002",
    "userdefinedPromotionalProductId": ""
  },
  "principalAmount": "$0.00"
}

```

### Error Response Payload

```json
{
  "errorCode": "V5PH0004SF",
  "errorMessage": "Get Request - Record Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get Request - Record Not Found |