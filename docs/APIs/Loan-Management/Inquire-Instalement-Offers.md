# Inquire Instalment Offers

This API is used to fetch instalment offers for a given loan plan id, Loan Amount and accountId/paymentInstrumentId.

## Endpoint

`GET /v1/loans/{accountId}/instalmentOffers`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable and loanAmount and loanPlanId should be sent as Query parameter.***

<!--
type: tab
-->

```json
{
    "instalmentOffers": [
        {
            "annualInterestRate": "11.00000%",
            "conversionFeeAmount": "$1.00",
            "instalmentAmount": "$16.67",
            "totalRepaymentAmount": "$100.00",
            "totalInterestAmount": "$0.00",
            "tenure": 6,
            "prorataInterestAmount": "$0.00"
        },
        {
            "annualInterestRate": "11.00000%",
            "conversionFeeAmount": "$12.00",
            "instalmentAmount": "$8.33",
            "totalRepaymentAmount": "$100.00",
            "totalInterestAmount": "$0.00",
            "tenure": 12,
            "prorataInterestAmount": "$0.00"
        }
    ],
    "loanPlanId": 8,
    "loanAmount": "$100.00"
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
    "instance": "/v1/loans/0007000011000000608/instalmentOffers",
    "invalid-params": [
      "V5LE4001ED: Account/ card number is not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/instalmentOffers).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId path variable. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `loanAmount` | Query Parameter | *string* | 17 | This field indicates amount which has to be converted to a Loan.|
| `loanPlanId` | Query Parameter | *number* | 5 | Identification number of the Credit Plan Master entity and Plan Number to which loan is to be converted.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LE4001EA` | Loan amount can not be zero |  
| `V5LE4002EA` | Plan number can not be zero |  
| `V5LE4003EA` | Account/ card number can not be spaces |
| `V5LE4001EB` | Business unit is not determined |
| `V5LE4001EC` | Business unit is not present in file |
| `V5LE4002EB` | Plan record not on file |
| `V5LE4001ED` | Account/ card number is not found |
| `V5LE4001EE` | Product not available on file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
