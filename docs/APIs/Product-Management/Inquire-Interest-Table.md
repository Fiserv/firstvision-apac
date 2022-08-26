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
  "includeBalanceFlagsForInterestCalculation": {
    "isInterestOnCollectionFeesEnabled": "1",
    "isInterestOnInsuranceEnabled": "0",
    "isInterestOnInterestEnabled": "0",
    "isInterestOnLateFeeEnabled": "1",
    "isInterestOnMembershipFeeEnabled": "1",
    "isInterestOnNsfFeeEnabled": "1",
    "isInterestOnOverLimitFeeEnabled": "0",
    "isInterestOnRecoveryFeeEnabled": "1",
    "isInterestOnServiceFeeEnabled": "1",
    "isInterestOnUserFee1Enabled": "0",
    "isInterestOnUserFee2Enabled": "0",
    "isInterestOnUserFee3Enabled": "0",
    "isInterestOnUserFee4Enabled": "0",
    "isInterestOnUserFee5Enabled": "0",
    "isInterestOnUserFee6Enabled": "0"
  },
  "interestCalculationOptions": {
    "accrualMethod": "D",
    "interestNextStatement": "D",
    "startInterestOnCreditTransaction": "P",
    "startInterestOnDebitTransaction": "T",
    "yearBase": "0"
  },
  "interestControls": {
    "allowNsfPaymentReversal": "0",
    "ceilingLimits": {
      "balanceLimit": "$0.00",
      "ceilingRate1": "99.99999%",
      "ceilingRate2": "99.99999%",
      "floorRate1": "0.00000%",
      "floorRate2": "0.00000%"
    },
    "examineCycleInterestVariance": "0",
    "interestRounding": "0"
  },
  "interestParametersForCombinedGraceAndCycleOptions": {
    "currentCycleBeginningThresholdAmount": "$0.00",
    "currentCycleEndingThresholdAmount": "$0.00",
    "currentCycleInterestBalanceIndicator": "0",
    "currentCyclePaidDateQualification": "0",
    "isCurrentCycleBeginBalanceEnabled": "0",
    "isCurrentCycleEndingBalanceEnabled": "0",
    "isCurrentCycleNsfPaymentReversalEnabled": "0",
    "isPriorCycleBeginBalanceEnabled": "0",
    "isPriorCycleEndingBalanceEnabled": "0",
    "isPriorCycleNsfPaymentReversalEnabled": "0",
    "isPriorDeferredBeginBalanceEnabled": "0",
    "isPriorDeferredEndingBalanceEnabled": "0",
    "isPriorDeferredNsfPaymentReversalEnabled": "0",
    "isResidualInterestBeginBalanceEnabled": "0",
    "isResidualInterestEndingBalanceEnabled": "0",
    "isResidualInterestNsfPaymentReversalEnabled": "0",
    "isWaiveCurrentCycleInterestEnabled": "0",
    "isWaivePriorCycleInterestEnabled": "0",
    "isWaivePriorDeferredInterestEnabled": "0",
    "isWaiveResidualInterestEnabled": "0",
    "priorCycleBeginningThresholdAmount": "$0.00",
    "priorCycleEndingThresholdAmount": "$0.00",
    "priorCycleInterestBalanceIndicator": "0",
    "priorCyclePaidDateQualification": 0,
    "priorDeferredBeginningThresholdAmount": "$0.00",
    "priorDeferredEndingThresholdAmount": "$0.00",
    "priorDeferredInterestBalanceIndicator": "0",
    "priorDeferredPaidDateQualification": "0",
    "residualInterestBalanceIndicator": 0,
    "residualInterestBeginningThresholdAmount": "$0.00",
    "residualInterestEndingThresholdAmount": "$0.00",
    "residualInterestPaidDateQualification": 0,
    "transactionQualification": "0"
  },
  "interestRates": {
    "limit1": "$999,999,999,999,999.00",
    "limit2": "$0.00",
    "limit3": "$0.00",
    "limit4": "$0.00",
    "limit5": "$0.00",
    "limit6": "$0.00",
    "limit7": "$0.00",
    "limit8": "$0.00",
    "rate1": "0.00000%",
    "rate2": "0.00000%",
    "rate3": "0.00000%",
    "rate4": "0.00000%",
    "rate5": "0.00000%",
    "rate6": "0.00000%",
    "rate7": "0.00000%",
    "rate8": "0.00000%",
    "rate9": "0.00000%",
    "rateIndexTable": "7",
    "rateType": "V",
    "tierLimitIndicator": "1",
    "variance1": "8.99000%",
    "variance2": "0.00000%",
    "variance3": "0.00000%",
    "variance4": "0.00000%",
    "variance5": "0.00000%",
    "variance6": "0.00000%",
    "variance7": "0.00000%",
    "variance8": "0.00000%",
    "variance9": "0.00000%"
  },
  "productId": 0,
  "tableId": 1,
  "tableName": "INTEREST RATE TABLE FOR CASH PLAN"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/products/0/interestTable",
    "invalid-params": [
      "V5RT0004SF: Get Request - Record not found"
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
| `V5RT0004SF` | Get request - Record Not Found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*