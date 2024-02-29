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
            "planStatus": 10,
            "referenceNumber": "202409300018",
            "closeReason": "0",
            "totalRepaymentAmount": "$106.62",
            "finalPaymentDate": "00/00/0000",
            "outstandingLoanAmount": "$0.00",
            "openDate": "01/10/2024",
            "annualPercentageRate": "1.20000%",
            "originalTerm": 12,
            "closeDate": "00/00/0000",
            "manualCloseIndicator": 0,
            "prorataInterestAmount": "$0.00",
            "instalmentAmount": "$0.00",
            "planSequenceNumber": 2,
            "planId": 5,
            "loanStatus": "A",
            "originalLoanAmount": "$100.00",
            "description": "EPP PLAN INTEREST BASED",
            "currentTerm": 0,
            "remainingTerm": 0,
            "typeOfLoan": 0,
            "conversionFeeAmount": "$0.00"
        },
        {
            "planStatus": 10,
            "referenceNumber": "202409300021",
            "closeReason": "0",
            "totalRepaymentAmount": "$205.87",
            "finalPaymentDate": "00/00/0000",
            "outstandingLoanAmount": "$0.00",
            "openDate": "01/10/2024",
            "annualPercentageRate": "1.00000%",
            "originalTerm": 6,
            "closeDate": "00/00/0000",
            "manualCloseIndicator": 0,
            "prorataInterestAmount": "$0.87",
            "instalmentAmount": "$0.00",
            "planSequenceNumber": 4,
            "planId": 5,
            "loanStatus": "A",
            "originalLoanAmount": "$200.00",
            "description": "RETAIL PLAN",
            "currentTerm": 0,
            "remainingTerm": 0,
            "typeOfLoan": 0,
            "conversionFeeAmount": "$0.00"
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
