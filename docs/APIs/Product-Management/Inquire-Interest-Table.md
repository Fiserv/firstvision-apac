# Inquire Interest Table

This service provides details of Interest Table. An Interest table identifies a set of parameters which include interest controls, interest rounding detail, interest calculation options, interest rates detail, balances for interest calculation and interest parameters for combined grace and cycle options.

## Endpoint

`GET /v1/products/{productId}/interestTable`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Business Unit/Table id and Product id should be sent as query and path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productId}/interestTable).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 001-998. | 
| `tableId` | Query parameter | *number* | 3 | Identification number of the product associated with this Interest table. | 
| `productId` | Path Variable | *number* | 3 | Unique identification number of the product associated with the organization. If the table is defined at organization level, populate this field as zeroes. For tables defined at product level, valid values are 001-998. | 

### Successful Response Payload

```json

{
  "businessUnit": 600,
  "productId": 0,
  "tableId": 1,
  "tableName": "INTEREST RATE TABLE FOR CASH PLAN",
  "interestControlsRes": {
    "interestRounding": "0",
    "examineCycleInterestVariance": "0",
    "allowNsfPaymentReversal": "0",
    "ceilingLimitsRes": {
      "floorRate1": "0.00000%",
      "ceilingRate1": "99.99999%",
      "floorRate2": "0.00000%",
      "ceilingRate2": "99.99999%",
      "balanceLimit": "$0.00"
    }
  },
  "interestCalculationOptionsRes": {
    "accrualMethod": "D",
    "yearBase": "0",
    "startInterestOnDebitTransaction": "P",
    "startInterestOnCreditTransaction": "T",
    "interestNextStatement": "C"
  },
  "interestRatesRes": {
    "tierLimitIndicator": "0",
    "rateType": "F",
    "rateIndexTable": 6,
    "rate7": "0.00000%",
    "variance7": "0.00000%",
    "limit7": "$0.00",
    "rate8": "0.00000%",
    "variance8": "0.00000%",
    "limit8": "$0.00",
    "rate9": "0.00000%",
    "variance9": "0.00000%",
    "rate1": "0.00000%",
    "variance1": "8.99000%",
    "limit1": "$999,999,999,999,999.00",
    "rate2": "0.00000%",
    "variance2": "0.00000%",
    "limit2": "$0.00",
    "rate3": "0.00000%",
    "variance3": "0.00000%",
    "limit3": "$0.00",
    "rate4": "0.00000%",
    "variance4": "0.00000%",
    "limit4": "$0.00",
    "rate5": "0.00000%",
    "variance5": "0.00000%",
    "limit5": "$0.00",
    "rate6": "0.00000%",
    "variance6": "0.00000%",
    "limit6": "$0.00"
  },
  "includeBalanceFlagsForInterestCalculationRes": {
    "isInterestOnMembershipFeeEnabled": "1",
    "isInterestOnInterestEnabled": "0",
    "isInterestOnServiceFeeEnabled": "1",
    "isInterestOnNsfFeeEnabled": "0",
    "isInterestOnOverLimitFeeEnabled": "1",
    "isInterestOnInsuranceEnabled": "0",
    "isInterestOnLateFeeEnabled": "1",
    "isInterestOnCollectionFeesEnabled": "0",
    "isInterestOnRecoveryFeeEnabled": "0",
    "isInterestOnUserFee1Enabled": "0",
    "isInterestOnUserFee2Enabled": "0",
    "isInterestOnUserFee3Enabled": "0",
    "isInterestOnUserFee4Enabled": "0",
    "isInterestOnUserFee5Enabled": "0",
    "isInterestOnUserFee6Enabled": "0"
  },
  "interestParametersForCombinedGraceAndCycleOptionsRes": {
    "transactionQualification": "0",
    "isWaivePriorDeferredInterestEnabled": "0",
    "isPriorDeferredNsfPaymentReversalEnabled": "0",
    "priorDeferredInterestBalanceIndicator": "0",
    "isPriorDeferredBeginBalanceEnabled": "0",
    "priorDeferredBeginningThresholdAmount": "$0.00",
    "isPriorDeferredEndingBalanceEnabled": "0",
    "priorDeferredEndingThresholdAmount": "$0.00",
    "priorDeferredPaidDateQualification": "0",
    "isWaiveCurrentCycleInterestEnabled": "0",
    "isCurrentCycleNsfPaymentReversalEnabled": "0",
    "currentCycleInterestBalanceIndicator": "0",
    "isCurrentCycleBeginBalanceEnabled": "0",
    "currentCycleBeginningThresholdAmount": "$0.00",
    "isCurrentCycleEndingBalanceEnabled": "0",
    "currentCycleEndingThresholdAmount": "$0.00",
    "currentCyclePaidDateQualification": "0",
    "isWaivePriorCycleInterestEnabled": "0",
    "isPriorCycleNsfPaymentReversalEnabled": "0",
    "priorCycleInterestBalanceIndicator": "0",
    "isPriorCycleBeginBalanceEnabled": "0",
    "priorCycleBeginningThresholdAmount": "$0.00",
    "isPriorCycleEndingBalanceEnabled": "0",
    "priorCycleEndingThresholdAmount": "$0.00",
    "priorCyclePaidDateQualification": "0",
    "isWaiveResidualInterestEnabled": "0",
    "isResidualInterestNsfPaymentReversalEnabled": "0",
    "residualInterestBalanceIndicator": 0,
    "isResidualInterestBeginBalanceEnabled": "0",
    "residualInterestBeginningThresholdAmount": "$0.00",
    "isResidualInterestEndingBalanceEnabled": "0",
    "residualInterestEndingThresholdAmount": "$0.00",
    "residualInterestPaidDateQualification": "0"
  }
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