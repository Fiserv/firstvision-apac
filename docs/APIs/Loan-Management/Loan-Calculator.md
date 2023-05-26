# Loan Calculator

This API is used to calculate the loan repayment options for prospective borrowers based on the details given input request.

## Endpoint

`POST /v1/loans/calculator`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "principalAmount": "600.00",
  "insuranceAmount": "500.00",
  "currencyCode": "036",
  "userFeeAmount": "300.00",
  "interestRate": 1400,
  "term": 10,
  "fixedPaymentAmount": "0.00",
  "isPaymentScheduledEnabled": 1,
  "interestMethod": 0,
  "roundingIndicator": 0
}
```

<!--
type: tab
-->

```json

{
  "loanCalculatorDetails": {
    "finalPaymentAmount": "$140.09",
    "fixedPaymentAmount": "$140.09",
    "insuranceAmount": "$500.00",
    "interestRate": "00014.00%",
    "term": 10,
    "principalAmount": "$600.00",
    "totalFinancedAmount": "$1,400.00",
    "totalInterestAmount": "$0.90",
    "totalLoanAmount": "$1,400.90",
    "userFeeAmount": "$300.00"
  },
  "loanScheduleAndMonthdetails": {
    "loanMethod": 0,
    "term": 10
  },
  "monthlyLoanPaymentDetails": [
    {
      "currentTerm": 1,
      "endingBalance": "$1,260.07",
      "finalAmount": "$139.93",
      "interestAmount": "$0.16"
    },
    {
      "currentTerm": 2,
      "endingBalance": "$1,120.13",
      "finalAmount": "$139.94",
      "interestAmount": "$0.15"
    },
    {
      "currentTerm": 3,
      "endingBalance": "$980.17",
      "finalAmount": "$139.96",
      "interestAmount": "$0.13"
    },
    {
      "currentTerm": 4,
      "endingBalance": "$840.19",
      "finalAmount": "$139.98",
      "interestAmount": "$0.11"
    },
    {
      "currentTerm": 5,
      "endingBalance": "$700.20",
      "finalAmount": "$139.99",
      "interestAmount": "$0.10"
    },
    {
      "currentTerm": 6,
      "endingBalance": "$560.19",
      "finalAmount": "$140.01",
      "interestAmount": "$0.08"
    },
    {
      "currentTerm": 7,
      "endingBalance": "$420.17",
      "finalAmount": "$140.02",
      "interestAmount": "$0.07"
    },
    {
      "currentTerm": 8,
      "endingBalance": "$280.13",
      "finalAmount": "$140.04",
      "interestAmount": "$0.05"
    },
    {
      "currentTerm": 9,
      "endingBalance": "$140.07",
      "finalAmount": "$140.06",
      "interestAmount": "$0.03"
    },
    {
      "currentTerm": 10,
      "endingBalance": "$0.00",
      "finalAmount": "$140.07",
      "interestAmount": "$0.02"
    }
  ]
}

```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/loans/calculator",
    "invalid-params": [
      "V5LC4001SK: CURRENCY CODE IS REQUIRED WHEN ROUNDING IND IS 3"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/loans/calculator).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `principalAmount` | Payload  | *number* | 17 | Principal balance of the loan in monetary units and subunits.|
| `currencyCode` | Payload  | *string* | 3 | ISO Standard Currency Code or ISO Country Code that identifies the unit of currency for this loan.|
| `fixedPaymentAmount` | Payload  | *number* | 17 | Amount of the fixed payment. This field is required if LOAN TERM is not supplied.|
| `term` | Payload  | *integer*| 3 | Term for the loan. This field is required if FIXED PAYMENT AMOUNT is not supplied.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LC4001SA` | Principle must be greater than zero |  
| `V5LC4001SB` | Insurance must be greater than or equal to zero |  
| `V5LC4001SC` | User fees must be greater than or equal to zero |  
| `V5LC4001SD` | Interest rate must be greater than or equal to zero |  
| `V5LC4001SE` | Loan term must be greater than or equal to zero |  
| `V5LC4001SF` | Principle amount is not numeric |  
| `V5LC4001SG` | Loan term or fixed payment must be greater than zero |  
| `V5LC4001SH` | Payment schedule incdicator must be 0 or 1 |  
| `V5LC4001SI` | Interest method must be 0 or 1 |  
| `V5LC4001SJ` | Rouding indicator must be 0 or 1 or 2 or 3 |  
| `V5LC4001SK` | Currency code is required when rounding ind is 3 |  
| `V5LC4001SL` | Invalid currency code |  
| `V5LC4001SM` | Can not process verify input values |  

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
