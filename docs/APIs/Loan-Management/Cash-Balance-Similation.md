# Cash Balance Simulation

This API is used to validate if the Cash balance simulation is allowed for given accountId/paymentInstrumentId. This API will be created to cater Simulation steps, depending on the Type of Request.

## Endpoint

`POST /v1/loans/cashBalanceSimulation`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 700,
  "accountId": "0007000011163060009",
  "loanPlanId": 10,
  "tenure": 6,
  "cashLoanAmount": "100.00",
  "authorizationCode": "12345",
  "annualPercentageRate": "0.00000"
}
```

<!--
type: tab
-->

```json
{
    "LoanScheduleDetails": [
        {
            "tenure": 0,
            "totalBalance": "$100.00",
            "principalAmount": "$0.00",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$10.00"
        },
        {
            "tenure": 1,
            "totalBalance": "$100.00",
            "principalAmount": "$16.67",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 2,
            "totalBalance": "$83.33",
            "principalAmount": "$16.67",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 3,
            "totalBalance": "$66.66",
            "principalAmount": "$16.67",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 4,
            "totalBalance": "$49.99",
            "principalAmount": "$16.67",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 5,
            "totalBalance": "$33.32",
            "principalAmount": "$16.67",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 6,
            "totalBalance": "$16.65",
            "principalAmount": "$16.65",
            "interestAmount": "$0.00",
            "conversionFeeAmount": "$0.00"
        }
    ],
    "instalmentDetails": {
        "totalRepaymentAmount": "$100.00",
        "totalInterestAmount": "$0.00",
        "conversionFeeAmount": "$10.00",
        "prorataInterestAmount": "$0.00",
        "instalmentAmount": "$16.67",
        "loanReferenceNumber": "",
        "totalPrincipalAmount": "$100.00",
        "planIdDescription": "CIP EPP PLAN FEE BASED"
    },
    "businessUnit": 700,
    "loanPlanId": 10,
    "planSequenceNumber": 1,
    "cashLoanAmount": "$100.00",
    "accountId": "0007000011163060009",
    "authorizationCode": "12345",
    "tenure": 7,
    "annualPercentageRate": "0.00000%"
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "442201",
        "detail": "Please refer to invalid-params for error details",
        "title": "Unprocessable Entity",
        "instance": "/v1/loans/cashBalanceSimulation",
        "source": "VPL",
        "status": 422,
        "invalid-params": [
            "V5LF4005EB: APR CAN NOT BE OVERRIDDEN"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/loans/cashBalanceSimulation).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload  | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId in request. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `loanPlanId` | Payload  | *integer* | 5 | Identification number of the Credit Plan Master entity. The values are 1–99998. You can establish as many as 99,998 Credit Plan Master entity for each organization.|
| `tenure` | Payload  | *integer* | 3 | Field indicates the term used while converting transaction into instalment.|
| `cashLoanAmount` | Payload  | *string* | 17 | Cash amount of the transaction.|
| `authorizationCode` | Payload  | *string* | 6 | Authorization code associated with the transaction.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LA4008EA` | Auth code can not be spaces or zeroes |  
| `V5LA4003EA` | Plan record not present in file |  
| `V5LA4007EA` | Cash loan amt should be between EPP min amount and EPP max amount |  
| `V5LA4003EB` | Invalid loan plan type |   
| `V5LA4001ED` | Account not found |  
| `V5LA4001EE` | Product not found  |  
| `V5LF4001EA` | Business unit is not determined |  
| `V5LF4001EB` | Business unit is not present in file |  
| `V5LF4001EC` | EPP active indicator is inactive at business unit level |  
| `V5LF4002EA` | Account / card number is not found |  
| `V5LF4001ED` | Product record not on file |  
| `V5LF4001EE` | EPP active indicator is inactive at product level |  
| `V5LF4001EF` | Loan feature is not allowed at product level |  
| `V5LF4003EA` | Plan record not on file |  
| `V5LF4003EB` | EPP is not active at plan level |  
| `V5LF4003EC` | Plan EPP effective date is greater than next processing date |  
| `V5LF4003ED` | Plan EPP end date is lesser than next processing date |  
| `V5LF4003EE` | Promo plan is required |  
| `V5LF4002EB` | EPP conversion not allowed, account delinquent |  
| `V5LF4002EC` | EPP conversion not allowed, invalid account status |  
| `V5LF4002ED` | EPP conversion not allowed, account blocked |  
| `V5LF4002EE` | Maximum plan number reached |  
| `V5LF4002EF` | Account / card number is required |  
| `V5LF4005EA` | APR can not be overridden |  
| `V5LF4004EA` | Term is required |  
| `V5LF4004EB` | Term is not present in EPP tier table in plan record |  
| `V5LF4006EA` | Loan amount is required |  
| `V5LF4005EB` | APR can not be overridden |  
| `V5LF4002EE` | Maximum plan number reached |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
