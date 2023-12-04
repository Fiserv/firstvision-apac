# List Loans By Account

This API is used to fetch list of loans associated with an account id given.

## Endpoint

`GET /v1/loans/{accountId}/listLoans`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable.***

<!--
type: tab
-->

```json
{
    "listLoans": [
        {
            "referenceNumber": "202409300018",
            "planStatus": 10,
            "closeReason": "0",
            "totalRepaymentAmount": "$106.62",
            "prorataInterestAmount": "$0.00",
            "instalmentAmount": "$0.00",
            "planSequence": 2,
            "planId": 5,
            "loanStatus": "A",
            "conversionFeeAmount": "$0.00",
            "closeDate": "00/00/0000",
            "typeOfLoan": 5,
            "openDate": "01/10/2024",
            "annualPercentageRate": "120000",
            "originalTerm": 12,
            "outstandingLoanAmount": "$0.00",
            "originalLoanAmount": "$100.00",
            "description": "EPP PLAN INTEREST BASED",
            "currentTerm": 0,
            "remainingTerm": 0,
            "manualCloseIndicator": 0,
            "finalPaymentDate": "00/00/0000"
        },
        {
            "referenceNumber": "202409300019",
            "planStatus": 10,
            "closeReason": " ",
            "totalRepaymentAmount": "$1,200,000,000,000.01",
            "prorataInterestAmount": "$0.00",
            "instalmentAmount": "0.00",
            "planSequence": 100,
            "planId": 3000,
            "loanStatus": "0",
            "conversionFeeAmount": "$0.00",
            "closeDate": "00/00/0000",
            "typeOfLoan": 5,
            "openDate": "20/07/4120",
            "annualPercentageRate": "0",
            "originalTerm": 0,
            "outstandingLoanAmount": "$0.00",
            "originalLoanAmount": "$276,200,000,000,000.01",
            "description": "EPP PLAN INTEREST BASED",
            "currentTerm": 120,
            "remainingTerm": 0,
            "manualCloseIndicator": 0,
            "finalPaymentDate": "00/00/0000"
        }
    ],
    "totalLoanCount": 3,
    "accountId": "0007000011000000616",
    "businessUnit": 700
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
    "instance": "/v1/loans/0007000011000000616/listLoans",
    "invalid-params": [
      "V5LI4002EB: Account number not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/listLoans).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LI4002EA` | Account number is space |  
| `V5LI4001EA` | Business unit is not determined |  
| `V5LI4002EB` | Account number not found |
| `V5LI4001EB` | Business unit is not present in file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
