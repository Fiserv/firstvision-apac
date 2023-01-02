# Loan Calculator

This Loan Calculator Service is used to calculate the loan repayment options for prospective borrowers. This function requires that you enter either the loan term or fixed payment amount. You can also enter other loan components, such as the interest rate, insurance, and user fees. When you press submit, CMS calculates and displays the loan term, fixed payment, final payment, total financed amount, total interest amount, and total loan amount.

## Endpoint

`POST /v1/loans/calculator`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "principalAmount": "60000",
  "insuranceAmount": "50000",
  "currencyCode": "036",
  "userFeeAmount": "30000",
  "interestRate": 1400,
  "tenure": 10,
  "fixedPaymentAmount": "0",
  "isPaymentScheduledEnabled": "1",
  "interestMethod": "0",
  "roundingIndicator": "0"
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
    "interestRate": "1400",
    "tenure": 10,
    "principalAmount": "$600.00",
    "totalFinancedAmount": "$1,400.00",
    "totalInterestAmount": "$0.90",
    "totalLoanAmount": "$1,400.90",
    "userFeeAmount": "$300.00"
  },
  "loanScheduleAndMonthdetails": {
    "loanMethod": 0,
    "tenure": 10
  },
  "monthlyLoanPaymentDetails": [
    {
      "currentTenure": 1,
      "endingBalance": "$1,260.07",
      "finalAmount": "$139.93",
      "intrestAmount": "$0.16"
    },
    {
      "currentTenure": 2,
      "endingBalance": "$1,120.13",
      "finalAmount": "$139.94",
      "intrestAmount": "$0.15"
    },
    {
      "currentTenure": 3,
      "endingBalance": "$980.17",
      "finalAmount": "$139.96",
      "intrestAmount": "$0.13"
    },
    {
      "currentTenure": 4,
      "endingBalance": "$840.19",
      "finalAmount": "$139.98",
      "intrestAmount": "$0.11"
    },
    {
      "currentTenure": 5,
      "endingBalance": "$700.20",
      "finalAmount": "$139.99",
      "intrestAmount": "$0.10"
    },
    {
      "currentTenure": 6,
      "endingBalance": "$560.19",
      "finalAmount": "$140.01",
      "intrestAmount": "$0.08"
    },
    {
      "currentTenure": 7,
      "endingBalance": "$420.17",
      "finalAmount": "$140.02",
      "intrestAmount": "$0.07"
    },
    {
      "currentTenure": 8,
      "endingBalance": "$280.13",
      "finalAmount": "$140.04",
      "intrestAmount": "$0.05"
    },
    {
      "currentTenure": 9,
      "endingBalance": "$140.07",
      "finalAmount": "$140.06",
      "intrestAmount": "$0.03"
    },
    {
      "currentTenure": 10,
      "endingBalance": "$0.00",
      "finalAmount": "$140.07",
      "intrestAmount": "$0.02"
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
| `tenure` | Payload  | *integer*| 3 | Term for the loan. This field is required if FIXED PAYMENT AMOUNT is not supplied.|



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