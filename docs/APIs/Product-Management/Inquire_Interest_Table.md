# Inquire Interest Table

 This service provides details of Interest Table. An Interest table identifies a set of parameters which include interest controls, interest rounding detail, interest calculation options, interest rates detail, balances for interest calculation and interest parameters for combined grace and cycle options.


## Endpoint

`GET /v1/products/{productNumber}/interestTable`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Business Unit/Table Number and Account Number should be sent as query and path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productNumber}/interestTable).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the business unit associated with this Interest table. | 
| `tableNumber` | Query parameter | *number* | 3 | Identification number of the product associated with this Interest table. | 
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account. | 

### Successful Response Payload

```json
{
  "interestControlsRes": {
    "ceilingLimitsRes": {
      "balanceLimit": "$0.00",
      "ceilingRate1": "99.99999%",
      "floorRate2": "0.00000%",
      "floorRate1": "0.00000%",
      "ceilingRate2": "99.99999%"
    },
    "interestRounding": "0",
    "allowNsfPaymentReversal": "0",
    "examineCycleInterestVariance": "0"
  },
  "interestCalculationOptionsRes": {
    "interestNextStatement": "D",
    "startInterestOnDebitTransaction": "T",
    "startInterestOnCreditTransaction": "P",
    "accrualMethod": "D",
    "yearBase": "0"
  },
  "interestRatesRes": {
    "tierLimitIndicator": "1",
    "limit8": "$0.00",
    "limit7": "$0.00",
    "rate8": "0.00000%",
    "variance8": "0.00000%",
    "variance7": "0.00000%",
    "rate9": "0.00000%",
    "rate7": "0.00000%",
    "variance9": "0.00000%",
    "rate1": "0.00000%",
    "limit1": "$999,999,999,999,999.00",
    "variance2": "0.00000%",
    "limit2": "$0.00",
    "rate2": "0.00000%",
    "rateIndexTable": 7,
    "rateType": "V",
    "variance1": "8.99000%",
    "rate3": "0.00000%",
    "rate5": "0.00000%",
    "variance5": "0.00000%",
    "limit4": "$0.00",
    "limit6": "$0.00",
    "variance4": "0.00000%",
    "rate6": "0.00000%",
    "limit5": "$0.00",
    "rate4": "0.00000%",
    "variance6": "0.00000%",
    "variance3": "0.00000%",
    "limit3": "$0.00"
  },
  "balancesForInterestCalculationRes": {
    "chargeInterestOnUserFee6": "0",
    "chargeInterestOnUserFee2": "0",
    "interestOnCollectionFees": "1",
    "chargeInterestOnInterest": "0",
    "chargeInterestOnUserFee4": "0",
    "interestOnNsfFee": "1",
    "chargeInterestOnUserFee5": "0",
    "chargeInterestOnService": "1",
    "chargeInterestOnInsurance": "0",
    "interestOnRecoveryFees": "1",
    "chargeInterestOnOverLimit": "0",
    "chargeInterestOnUserFee1": "0",
    "interestOnLateCharge": "1",
    "chargeInterestOnMembership": "1",
    "chargeInterestOnUserFee3": "0"
  },
  "interestParametersForCombinedGraceAndCycleOptionsRes": {
    "useResidualInterestBeginBalance": "0",
    "usePriorDeferredNsfPaymentReversal": "0",
    "transactionQualification": "0",
    "priorDeferredEndBalanceThreshold": "$0.00",
    "priorDeferredPaidDateQualification": "0",
    "waiveCurrentCycleInterest": "0",
    "usePriorDeferredEndingBalance": "0",
    "currentCycleInterestBalanceIndicator": "0",
    "waivePriorDeferredInterest": "0",
    "priorDeferredInterestBalanceIndicator": "0",
    "usePriorDeferredBeginBalance": "0",
    "priorDeferredBeginBalanceThreshold": "$0.00",
    "useCurrentCycleNsfPaymentReversal": "0",
    "residualInterestBalanceIndicator": 0,
    "priorCycleInterestBalanceIndicator": "0",
    "residualInterestBeginBalanceThreshold": "$0.00",
    "residualInterestPaidDateQualification": "0",
    "residualInterestEndBalanceThreshold": "$0.00",
    "waiveResidualInterest": "0",
    "useCurrentCycleEndingBalance": "0",
    "currentCyclePaidDateQualification": "0",
    "currentCycleBeginBalanceThreshold": "$0.00",
    "priorCycleBeginBalanceThreshold": "$0.00",
    "usePriorCycleEndingBalance": "0",
    "priorCyclePaidDateQualification": "0",
    "waivePriorCycleInterest": "0",
    "usePriorCycleBeginBalance": "0",
    "usePriorCycleNsfPaymentReversal": "0",
    "priorCycleEndBalanceThreshold": "$0.00",
    "useCurrentCycleBeginBalance": "0",
    "useResidualInterestEndingBalance": "0",
    "useResidualInterestNsfPaymentReversal": "0",
    "currentCycleEndBalanceThreshold": "$0.00"
  },
  "businessUnit": 600,
  "productNumber": 0,
  "tableNumber": 1,
  "tableName": "INTEREST RATE TABLE FOR CASH PLAN"
}

```

### Error Response Payload

```json
{
  "errorCode": "V5RT0004SF",
  "errorMessage": "Get Request - Record Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5RT0004SF` | Get Request - Record Not Found |