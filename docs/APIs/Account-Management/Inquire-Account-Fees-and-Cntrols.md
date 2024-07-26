# Inquire Account Fees and Controls

The API provides various fees and fee controls along with other miscellaneous details defined from account level, product level and fee control table for a specific account id.

## Endpoint

`GET /v1/accounts/{accountId}/feesAndControls`

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
  "serviceFeeWaiversAtAccount" : {
    "isWaiveFee01Enabled" : 0,
    "isWaiveFee02Enabled" : 0,
    "isWaiveFee03Enabled" : 0,
    "isWaiveFee04Enabled" : 0,
    "isWaiveFee05Enabled" : 0,
    "isWaiveFee06Enabled" : 0,
    "isWaiveFee07Enabled" : 0,
    "isWaiveFee08Enabled" : 0,
    "isWaiveFee09Enabled" : 0,
    "isWaiveFee10Enabled" : 0,
    "isWaiveFee11Enabled" : 0,
    "isWaiveFee12Enabled" : 0,
    "isWaiveFee13Enabled" : 0,
    "isWaiveFee14Enabled" : 0,
    "isWaiveFee15Enabled" : 0,
    "isWaiveFee16Enabled" : 0,
    "isWaiveFee17Enabled" : 0,
    "isWaiveFee18Enabled" : 0,
    "isWaiveFee19Enabled" : 0,
    "isWaiveFee20Enabled" : 0,
    "isWaiveFee21Enabled" : 0,
    "isWaiveFee22Enabled" : 0,
    "isWaiveFee23Enabled" : 0,
    "isWaiveFee24Enabled" : 0,
    "isWaiveFee25Enabled" : 0
  },
  "cashAdvanceFeeWaiversAtAccount" : {
    "isWaiveFee1Enabled" : 0,
    "isWaiveFee2Enabled" : 0,
    "isWaiveFee3Enabled" : 0,
    "isWaiveFee4Enabled" : 0,
    "isWaiveFee5Enabled" : 0
  },
  "miscWaiversAtAccount" : {
    "isWaiveLateChargeEnabled" : 0,
    "isWaiveAnnualMembershipFeeEnabled" : 0,
    "isWaiveOverlimitFeeEnabled" : 0,
    "isWaiveNsf1-5FeeEnabled" : 0,
    "isWaiveInterestFeeEnabled" : 0,
    "isWaiveAddOnMembershipFeeEnabled" : 0
  },
  "membershipFeeControlsAtFeeTable" : {
    "supplementaryMembershipFeeAmount" : "$20.00",
    "supplementaryMembershipFeeRate" : "0.00000%",
    "membershipFeeFrequency" : 0,
    "expenditureThresholdAmountOrNumber" : 3000,
    "expenditureActualAmountOrNumber" : 0,
    "initialMembershipFeeAction" : 0,
    "initialMembershipFeeAmount" : "$20.00",
    "expenditureThresholdIndicator" : 1,
    "renewalMembershipFeeAction" : 0,
    "initialMembershipFeeRate" : "0.00000%",
    "renewalMembershipFeeAmount" : "$20.00",
    "renewalMembershipFeeRate" : "0.00000%",
    "supplementarymembershipFeeMethod" : 0,
    "waiveMembershipFeeIndicator" : 0,
    "refundMembershipFeeIndicator" : 0
  },
  "lateFeeControlsAtFeeTable" : {
    "cycleDueAmount1" : "$50.00",
    "cycleDueRate1" : "0.00000%",
    "cycleDueAmount2" : "$50.00",
    "cycleDueRate2" : "0.00000%",
    "cycleDueAmount3" : "$50.00",
    "cycleDueRate3" : "0.00000%",
    "cycleDueAmount4" : "$50.00",
    "cycleDueRate4" : "0.00000%",
    "cycleDueAmount5" : "$50.00",
    "cycleDueRate5" : "0.00000%",
    "cycleDueAmount6" : "$50.00",
    "cycleDueRate6" : "0.00000%",
    "cycleDueAmount7" : "$50.00",
    "cycleDueRate7" : "0.00000%",
    "cycleDueAmount8" : "$2.00",
    "cycleDueRate8" : "0.00000%",
    "cycleDueAmount9" : "$2.00",
    "cycleDueRate9" : "0.00000%",
    "cycleDue" : "7",
    "startAtCycleDue" : 1,
    "action" : "F"
  },
  "overlimitFeeControlsAtFeeTable" : {
    "action" : "F",
    "rate" : "0.00000%",
    "thresholdRate" : "0.00100%",
    "amount" : "$3.00"
  },
  "serviceFeeControlsAtFeeTable" : [ {
    "initiatingTransactionCode" : 6505,
    "tier1FeeAmountOrPercentage" : "$0.50",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 6506,
    "tier1FeeAmountOrPercentage" : "$2,500.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 800,
    "tier1FeeAmountOrPercentage" : "$25.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "2",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  }, {
    "initiatingTransactionCode" : 0,
    "tier1FeeAmountOrPercentage" : "$0.00",
    "transactionLimit" : 0,
    "method" : "1",
    "tier2FeeAmountOrPercentage" : "$0.00"
  } ],
  "cashAdvanceFeeControlsAtFeeTable" : [ {
    "transactionCode" : 700,
    "amount" : "$15.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 705,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "G"
  }, {
    "transactionCode" : 706,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "G"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  } ],
  "nonSufficientFeeControlsAtFeeTable" : [ {
    "transactionCode" : 8522,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  }, {
    "transactionCode" : 0,
    "amount" : "$0.00",
    "rate" : "0.00000%",
    "action" : "F"
  } ],
  "userFeeControlsAtFeeTable" : [ {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  }, {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  }, {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  }, {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  }, {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  }, {
    "action" : "F",
    "rate" : "0.00000%",
    "amount" : "$0.00",
    "description" : " "
  } ],
  "blockCodeControlsAtProduct" : [ {
    "isWaiveOverlimitFeeEnabled" : "Y",
    "isWaiveNSFChequeFeeEnabled" : "N",
    "waiveMembershipFeeIndicator" : 0,
    "isWaiveFinanceChargeEnabled" : "0",
    "blockCode" : "F",
    "isWaiveLateChargeEnabled" : "N"
  }, {
    "isWaiveOverlimitFeeEnabled" : "Y",
    "isWaiveNSFChequeFeeEnabled" : "N",
    "waiveMembershipFeeIndicator" : 0,
    "isWaiveFinanceChargeEnabled" : "0",
    "blockCode" : "O",
    "isWaiveLateChargeEnabled" : "N"
  } ],
  "miscDetails" : {
    "defaultCashInterestRate" : "19.00000%",
    "defaultRetailInterestRate" : "20.90000%",
    "defaultPromoInterestRate" : "0.00000%",
    "issuanceId" : "B03",
    "cashPlanId" : 10000,
    "promoPlanId" : 0,
    "retailPlanId" : 20000
  },
  "userFeeWaiversAtAccount" : {
    "isWaiveFee2Enabled" : 0,
    "isWaiveFee3Enabled" : 0,
    "isWaiveFee4Enabled" : 0,
    "isWaiveFee5Enabled" : 0,
    "isWaiveFee6Enabled" : 0,
    "isWaiveFee1Enabled" : 0
  },
  "businessUnit" : 700,
  "accountId" : "0007000011009587504"
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
    "instance": "/v1/accounts/000200001000040329A/feesAndControls",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/feesAndControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
