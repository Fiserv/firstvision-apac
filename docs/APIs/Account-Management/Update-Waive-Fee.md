# Update Waive Fee

The account fee waive flags update service is used to update flag for waive intrest, user fees, waive tax calculation, waive letter fee, service fees, cash advance fees etc.

## Endpoint

`PUT /v1/accounts/{accountId}/waiveFee`

## Payload Example

### Request Payload

```json

{
  "isWaiveLateChargeEnabled": "1",
  "isWaiveInterestFeeEnabled": "1",
  "isWaiveAnnualMembershipFeeEnabled": "0",
  "isWaiveOverlimitFeeEnabled": "0",
  "isWaiveNsf1-5FeeEnabled": "3",
  "isWaiveCardIssuanceFeeEnabled": "1",
  "isWaiveLetterFeeEnabled": "1",
  "isWaiveAddOnMembershipFeeEnabled": "0",
  "isWaiveTaxEnabled": "1",
  "isWaiveCycleSpendFeeEnabled": "1",
  "UserFees": {
    "isWaiveFee1Enabled": "1",
    "isWaiveFee2Enabled": "1",
    "isWaiveFee3Enabled": "1",
    "isWaiveFee4Enabled": "1",
    "isWaiveFee5Enabled": "0",
    "isWaiveFee6Enabled": "0"
  },
  "CashAdvanceFees": {
    "isWaiveFee1Enabled": "1",
    "isWaiveFee2Enabled": "1",
    "isWaiveFee3Enabled": "1",
    "isWaiveFee4Enabled": "1",
    "isWaiveFee5Enabled": "1"
  },
  "ServiceFees": {
    "isWaiveFee01Enabled": "1",
    "isWaiveFee10Enabled": "1",
    "isWaiveFee11Enabled": "1",
    "isWaiveFee12Enabled": "1",
    "isWaiveFee13Enabled": "1",
    "isWaiveFee14Enabled": "1",
    "isWaiveFee15Enabled": "1",
    "isWaiveFee16Enabled": "1",
    "isWaiveFee17Enabled": "1",
    "isWaiveFee18Enabled": "1",
    "isWaiveFee19Enabled": "1",
    "isWaiveFee02Enabled": "1",
    "isWaiveFee20Enabled": "1",
    "isWaiveFee21Enabled": "1",
    "isWaiveFee22Enabled": "1",
    "isWaiveFee23Enabled": "1",
    "isWaiveFee24Enabled": "1",
    "isWaiveFee25Enabled": "1",
    "isWaiveFee03Enabled": "1",
    "isWaiveFee04Enabled": "1",
    "isWaiveFee05Enabled": "1",
    "isWaiveFee06Enabled": "1",
    "isWaiveFee07Enabled": "1",
    "isWaiveFee08Enabled": "1",
    "isWaiveFee09Enabled": "1"
  }
}
```

### Minimum	Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/waiveFee).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountid` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json

{
  "CashAdvanceFees": {
    "isWaiveFee1Enabled": "1",
    "isWaiveFee2Enabled": "1",
    "isWaiveFee3Enabled": "1",
    "isWaiveFee4Enabled": "1",
    "isWaiveFee5Enabled": "1"
  },
  "ServiceFees": {
    "isWaiveFee01Enabled": "1",
    "isWaiveFee02Enabled": "1",
    "isWaiveFee03Enabled": "1",
    "isWaiveFee04Enabled": "1",
    "isWaiveFee05Enabled": "1",
    "isWaiveFee06Enabled": "1",
    "isWaiveFee07Enabled": "1",
    "isWaiveFee08Enabled": "1",
    "isWaiveFee09Enabled": "1",
    "isWaiveFee10Enabled": "1",
    "isWaiveFee11Enabled": "1",
    "isWaiveFee12Enabled": "1",
    "isWaiveFee13Enabled": "1",
    "isWaiveFee14Enabled": "1",
    "isWaiveFee15Enabled": "1",
    "isWaiveFee16Enabled": "1",
    "isWaiveFee17Enabled": "1",
    "isWaiveFee18Enabled": "1",
    "isWaiveFee19Enabled": "1",
    "isWaiveFee20Enabled": "1",
    "isWaiveFee21Enabled": "1",
    "isWaiveFee22Enabled": "1",
    "isWaiveFee23Enabled": "1",
    "isWaiveFee24Enabled": "1",
    "isWaiveFee25Enabled": "1"
  },
  "UserFees": {
    "isWaiveFee1Enabled": "1",
    "isWaiveFee2Enabled": "1",
    "isWaiveFee3Enabled": "1",
    "isWaiveFee4Enabled": "1",
    "isWaiveFee5Enabled": "0",
    "isWaiveFee6Enabled": "0"
  },
  "accountId": "0006000011000000178",
  "businessUnit": 600,
  "isWaiveAddOnMembershipFeeEnabled": "0",
  "isWaiveAnnualMembershipFeeEnabled": "0",
  "isWaiveCardIssuanceFeeEnabled": "1",
  "isWaiveCycleSpendFeeEnabled": "1",
  "isWaiveInterestFeeEnabled": "1",
  "isWaiveLateChargeEnabled": "1",
  "isWaiveLetterFeeEnabled": "1",
  "isWaiveNsf1-5FeeEnabled": "3",
  "isWaiveOverlimitFeeEnabled": "0",
  "isWaiveTaxEnabled": "1"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS1002SV",
  "errorMessage": "Invalid  Waive Late Change"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0302SA` | Issuance ID must be equal to PERM issuance ID on logo |         
| `V5BS1002SA` | Relationship does not allow ACCT level change for late charge |
| `V5BS1002SV` | Invalid  Waive Late Change |
| `V5BS1001SV` | Invalid  Waive Interest Change |
| `V5BS1004SA` | Fee must be waived off for |
| `V5BS1006SV` | Invalid  Waive Overlimit |
| `V5BS1008SA` | Invalid  Waive Card Fee Indicator |
| `V5BS1010SV` | Invalid  Waive Card Fee Indicator |
| `V5BS1005SV` | Invalid  Waive Letter Change |
| `V5BS1012SV` | Invalid  Waive User Fee 1 |
| `V5BS1013SV` | Invalid  Waive User Fee 2 |
| `V5BS1014SV` | Invalid  Waive User Fee 3 |
| `V5BS1015SV` | Invalid  Waive User Fee 4 |
| `V5BS1016SV` | Invalid  Waive User Fee 5 |
| `V5BS1017SV` | Invalid  Waive User Fee 6 |
| `V5BS1030SV` | Invalid  Waive Suppress Member Fee |
| `V5BS1031SV` | Invalid  Waive Tax Calculation |
| `V5BS1009SV` | Invalid  Waive Svc Change |
| `V5BS1011SV` | Invalid  Waive Cash Adverse Fee |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*