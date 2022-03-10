# Update Waive Fee

The account fee waive flags update service is used to update flag for waive intrest, user Fee 1/2/3/4/5/6, waive tax calculation, waive letter fee, service fee, cash advance fee etc.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.
  
## Endpoint

`PUT /v1/accounts/{accountNumber}/waiveFee`

## Payload Example

### Request Payload

```json
{
  "waiveInterest": 1,
  "userFees5": 0,
  "userFees4": 1,
  "suppressMembershipFee": 0,
  "userFees6": 0,
  "userFees1": 0,
  "waiveOverlimitFee": 0,
  "userFees3": "string",
  "userFees2": 1,
  "waiveTaxCalculation": 1,
  "waiveMembership": 0,
  "waiveLateCharges": 1,
  "waiveCardIssuanceFees": 1,
  "waiveNSF15Fees": 3,
  "waiveLetterFee": 1,
  "serviceFees": [
    {
      "serviceFees1": "string"
    }
  ],
  "cashAdvanceFees": [
    {
      "waiveCashAdvance1": "string"
    }
  ]
}
```

### Minimum	Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/waiveFee).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 
| `product` | Payload | *number* | 1 |  Identification number of prodcust associated with account. | 
| `waiveLateCharges` | Payload | *string* | 1 | Waive Late Charges. | 
| `waiveInterest` | Payload | *string* | 1 | Waive Interest. | 
| `waiveMembership` | Payload | *string* | 1 | Waive Membership. | 
| `waiveOverlimitFee` | Payload | *string* | 1 | Waive Overlimit Fee | 
| `waiveNSF1-5Fee` | Payload | *string* | 1 | Waive NSF 1-5 Fees. | 
| `waiveCardIssuanceFees` | Payload | *string* | 1 | Waive Card Issuance Fee. |
| `waiveLetterFee` | Payload | *string* | 1 | Waive Letter Fee. |
| `waiveUserFee1-6` | Payload | *string* | 1 | Waive User Fee 1-6. |
| `suppressMembershipFee` | Payload | *string* | 1 | Supress Membership Fee. |
| `waiveTaxCalculation` | Payload | *string* | 1 | Waive Tax Calculation Fee. |
| `serviceFees1-25` | Payload | *string* | 1 | Service Fees. |
| `waiveCashAdvance1-5` | Payload | *string* | 1 | Waive Cash Advance Fee. |

### Successful Response Payload

```json

{
  "accountNumber": "0000000001000000115",
  "billingAcctInd": "0",
  "businessUnit": "600",
  "product": "600",
  "suppressMembershipFee": "0",
  "table2": [
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    },
    {
      "serviceFees1": "0"
    }
  ],
  "table4": [
    {
      "waiveCashAdvance1": "0"
    },
    {
      "waiveCashAdvance1": "0"
    },
    {
      "waiveCashAdvance1": "0"
    },
    {
      "waiveCashAdvance1": "0"
    },
    {
      "waiveCashAdvance1": "0"
    }
  ],
  "userFees1": "0",
  "userFees2": "1",
  "userFees3": "0",
  "userFees4": "1",
  "userFees5": "0",
  "userFees6": "0",
  "waiveCardIssuanceFees": "1",
  "waiveInterest": "1",
  "waiveLateCharges": "1",
  "waiveLetterFee": "1",
  "waiveMembership": "0",
  "waiveNSF15Fees": "3",
  "waiveOverlimitFee": "0",
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
