# Update Waive Fee

The account fee waive flags update service is used to update flag for waive intrest, user Fee 1/2/3/4/5/6, waive tax calculation, waive letter fee, service fee, cash advance fee etc.

## Endpoint

`PUT /v1/accounts/{accountNumber}/waiveFee`

## Payload Example

### Request Payload

```json
{
  "waiveLateCharges": "1",
  "waiveInterest": "1",
  "waiveMembership": "0",
  "waiveOverlimitFee": "0",
  "waiveNsf15Fees": "3",
  "waiveCardIssuanceFees": "1",
  "waiveLetterFee": "1",
  "userFees1": "0",
  "userFees2": "1",
  "userFees3": "1",
  "userFees4": "1",
  "userFees5": "0",
  "userFees6": "0",
  "suppressMembershipFee": "0",
  "waiveTaxCalculation": "1",
  "waiveCashAdvanceFeeGroupReq": {
    "waiveCashAdvance1": "1",
    "waiveCashAdvance2": "1",
    "waiveCashAdvance3": "1",
    "waiveCashAdvance4": "1",
    "waiveCashAdvance5": "1"
  },
  "waiveServiceFeeGroupReq": {
    "serviceFee1": "1",
    "serviceFee10": "1",
    "serviceFee11": "1",
    "serviceFee12": "1",
    "serviceFee13": "1",
    "serviceFee14": "1",
    "serviceFee15": "1",
    "serviceFee16": "1",
    "serviceFee17": "1",
    "serviceFee18": "1",
    "serviceFee19": "1",
    "serviceFee2": "1",
    "serviceFee20": "1",
    "serviceFee21": "1",
    "serviceFee22": "1",
    "serviceFee23": "1",
    "serviceFee24": "1",
    "serviceFee25": "1",
    "serviceFee3": "1",
    "serviceFee4": "1",
    "serviceFee5": "1",
    "serviceFee6": "1",
    "serviceFee7": "1",
    "serviceFee8": "1",
    "serviceFee9": "1"
  }
}
```

### Minimum	Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/waiveFee).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000178",
  "businessUnit": 600,
  "product": 1,
  "suppressMembershipFee": "0",
  "userFees1": "0",
  "userFees2": "1",
  "userFees3": "1",
  "userFees4": "1",
  "userFees5": "0",
  "userFees6": "0",
  "waiveCardIssuanceFees": "1",
  "waiveCashAdvanceFeeGroupRes": {
    "waiveCashAdvance1": "1",
    "waiveCashAdvance2": "1",
    "waiveCashAdvance3": "1",
    "waiveCashAdvance4": "1",
    "waiveCashAdvance5": "1"
  },
  "waiveInterest": "1",
  "waiveLateCharges": "1",
  "waiveLetterFee": "1",
  "waiveMembership": "0",
  "waiveNsf15Fees": "3",
  "waiveOverlimitFee": "0",
  "waiveServiceFeeGroupRes": {
    "serviceFee1": "1",
    "serviceFee10": "1",
    "serviceFee11": "1",
    "serviceFee12": "1",
    "serviceFee13": "1",
    "serviceFee14": "1",
    "serviceFee15": "1",
    "serviceFee16": "1",
    "serviceFee17": "1",
    "serviceFee18": "1",
    "serviceFee19": "1",
    "serviceFee2": "1",
    "serviceFee20": "1",
    "serviceFee21": "1",
    "serviceFee22": "1",
    "serviceFee23": "1",
    "serviceFee24": "1",
    "serviceFee25": "1",
    "serviceFee3": "1",
    "serviceFee4": "1",
    "serviceFee5": "1",
    "serviceFee6": "1",
    "serviceFee7": "1",
    "serviceFee8": "1",
    "serviceFee9": "1"
  },
  "waiveTaxCalculation": "1"
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