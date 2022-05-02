# Inquire Account Plan

This service will retrieve the plan detail as per the account number given in request.

## Endpoint

`GET /v1/accounts/{accountNumber}/inquirePlan`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/inquirePlan).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account.|

### Successful Response Payload

```json
{
  "accountNumber": "0002000010000400044",
  "beginningBalance": "$0.00",
  "billedNotPaidRes": {
    "annualFeeBilledNotPaidAmount": "$0.00",
    "collectionFeesBilledNotPaidAmount": "$0.00",
    "insuranceBilledNotPaidAmount": "$0.00",
    "interestBilledNotPaidAmount": "$0.00",
    "lateChargeBilledNotPaidAmount": "$0.00",
    "nsfBilledNotPaidAmount": "$0.00",
    "overlimitFeeBilledNotPaidAmount": "$0.00",
    "principalBalance": "$0.00",
    "recoveryFeesBilledNotPaidAmount": "$0.00",
    "serviceChargeBilledNotPaidAmount": "$0.00",
    "userFee1BilledNotPaidAmount": "$0.00",
    "userFee2BilledNotPaidAmount": "$0.00",
    "userFee3BilledNotPaidAmount": "$0.00",
    "userFee4BilledNotPaidAmount": "$0.00",
    "userFee5BilledNotPaidAmount": "$0.00",
    "userFee6BilledNotPaidAmount": "$0.00"
  },
  "businessUnit": 200,
  "dateLastMaintenance": "00/00/0000",
  "datesRes": {
    "accruedThroughDate": "31/12/2020",
    "billingBeginningDate": "00/00/0000",
    "dateLastPayment": "00/00/0000",
    "effectiveDate": "01/03/2021",
    "effectiveRateChangeDate": "00/00/0000",
    "insuranceAssessmentStartDate": "00/00/0000",
    "interestAssessmentStartDate": "00/00/0000",
    "paidOutDate": "00/00/0000",
    "paymentBeginningDate": "00/00/0000",
    "paymentTypeIndicatorMaintenanceDate": "00/00/0000",
    "planDate": "01/03/2021",
    "userFee1assessmentdate": "00/00/0000",
    "userFee2assessmentdate": "00/00/0000",
    "userFee3assessmentdate": "00/00/0000"
  },
  "disputedAmount": "$0.00",
  "generalDataRes": {
    "addonIndicator": "Y",
    "consolidatePaymentsIndicator": "N",
    "consolidateStatementsIndicator": "Y",
    "limitIndicator": 0,
    "planDescription": "",
    "rateType": "",
    "referenceNumber": ""
  },
  "itoDataRes": {
    "interestTableOverrideExpiryDate": "00/00/0000",
    "interestTableOverrideNumber": 0,
    "interestTableOverrideStatus": ""
  },
  "lastInterestRate": "0.00000%",
  "miscellenousDataRes": {
    "balanceTransferMonthsRemaining": 0,
    "cycletodatePaymentsPosted": "$0.00",
    "disclosureDays": 0,
    "fixedPaymentAmount": "$0.00",
    "interestExpiryDisclosureIndicator": "0",
    "lastInterestRateTableUsed": 0,
    "lastPaymentAmount": "$0.00",
    "lastPurchaseBalanceAmount": "$1.00",
    "lifetodatePaymentAmountsApplied": "$0.00",
    "lifetodatePaymentAmountsRequested": "$0.00",
    "lifetodateReturnsAmount": "$0.00",
    "paymentLastRequested": "$0.00",
    "paymentType": "T",
    "planNumberForConsolidatedPayments": 10002,
    "planSegmentTotalAmountDue": "$0.00",
    "planStatus": 1,
    "planStatusChangeDate": "00/00/0000",
    "planType": "R",
    "previousFixedPaymentAmount": "$0.00",
    "previousPlanStatus": 0,
    "rateTableOccurrenceIndicator": 2,
    "userdefinedProductCode": "10002",
    "userdefinedPromotionalProductId": ""
  }
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

