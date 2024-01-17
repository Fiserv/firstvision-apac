# Inquire Payoff Quote

This API is used to fetch Instalment plan balance and pro rata interest that would be charged in case the customer wants to close a Loan plan on a given date.
  
## Endpoint

`GET /v1/loans/{accountId}/payoffQuote`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable and loanPlanId, planSequenceNumber should be sent as query parameter.***

<!--
type: tab
-->

```json
{
    "planSequenceNumber": 2,
    "payoffDate": "17/02/2025",
    "nextStatementDate": "25/02/2025",
    "outstandingBalance": "$1,000.00",
    "prorataInterestAmount": "$0.71",
    "payoffQuoteAmount": "$1,000.71",
    "loanPlanId": 30101,
    "loanReferenceNumber": "202502150007",
    "accountId": "0007000011001690504",
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
    "instance": "/v1/loans/0007000011001690504/payoffQuote",
    "invalid-params": [
      "XXXXXXXXX: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/payoffQuote).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `loanPlanId` | Query Parameter  | *integer* | 05 | Identification number of the Credit Plan Master entity.|
| `planSequenceNumber` | Query Parameter | *integer* | 03 | Sequence number to identify the entity uniquely.|



### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `xxxxxxxxx` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
