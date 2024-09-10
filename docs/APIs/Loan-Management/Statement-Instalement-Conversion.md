# Statement Balance Conversion

This API is used to convert statement balance into Instalments for a given accountId/paymentInstrumentId. API first validates the given plans are eligible for statement balance conversion, if eligible then system converts into instalment for the requested term and also responds with loan scheduling details.

## Endpoint

`POST /v1/loans/statementBalanceConversion`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "accountId": "0006000011000000509",
  "annualPercentageRate": "0.00000",
  "businessUnit": 600,
  "loanPlanId": 10012,
  "statementInstalmentRequestedAmount": "100.00",
  "tenure": 12
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000509",
  "annualPercentageRate": "0.00000%",
  "businessUnit": 600,
  "instalmentDetails": {
    "conversionFeeAmount": "$2.00",
    "instalmentAmount": "$130.00",
    "loanReferenceNumber": "LN1238457389475",
    "planIdDescription": "RETAIL PLAN",
    "prorataInterestAmount": "$12.00",
    "totalInterestAmount": "$10.00",
    "totalPrincipalAmount": "$120.00",
    "totalRepaymentAmount": "$100.00"
  },
  "loanPlanId": 10012,
  "loanScheduleDetails": [
    {
      "conversionFeeAmount": "$5.00",
      "interestAmount": "$12.00",
      "principalAmount": "$1,500.00",
      "tenure": 12,
      "totalBalance": "$1,200.00"
    }
  ],
  "planDetails": [
    {
      "conversionAmount": "$100.00",
      "planId": 1,
      "planSequenceNumber": 1
    }
  ],
  "planSequenceNumber": 1,
  "qualificationGraceBalance": "$100.00",
  "statementInstalmentConvertedAmount": "$100.00",
  "statementInstalmentRequestedAmount": "$100.00",
  "tenure": 12
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
    "instance": "/v1/loans/statementBalanceConversion",
    "invalid-params": [
      "V5LS4010EA: CONVERSION AMOUNT SHOULD BE GREATER THAN ZERO"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]

```


<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/loans/statementBalanceConversion).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId in request. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `loanPlanId` | Payload  | *integer* | 05 | Identification number of the Credit Plan Master entity.|
| `tenure` | Payload | *integer* | 03 | Field indicates the term used while converting transaction into instalment.|
| `statementInstalmentRequestedAmount` | Payload | *string* | 17 | Amount requested for instalment conversion.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LS4010EB` | Loan conversion amount sould be within the EPP min amount and EPP max amount defined at loan plan |  
| `V5LS4007EA` | Invalid plan number |  
| `V5LS4008EA` | Invalid plan sequence |  
| `V5LS4010EA` | Conversion amount should be greater than zero |  
| `V5LS4001EE` | Business |  
| `V5LS4003EB` | Promo plan number not found in plan segment file |  
| `V5LS4007EB` | Plan number not found in plan segment file |  
| `V5LS4007EC` | Plan number should have statement balance loan conversion eligibility |  
| `V5LS4008EB` | Plan sequence number not found in plan segment file |  
| `V5LS4010EC` | Conversion amount for individual plans should not exceed the sip eligible balance for the corresponding plan |  
| `V5LS4001EA` | AMPS plan write - duplicate record found |  
| `V5LS4001EB` | AMPS loan write - duplicate record found |  
| `V5LS4001EC` | AMLS write - duplicate record found |  
| `V5LS4002EA` | Account not found |  
| `V5LS4001ED` | Business unit is not present in file |  
| `V5LS4011EB` | Number of plan and count of plan mismatch |  
| `V5LS4011EA` | Number of plan should not be greater than 5 |  
| `V5LS4003EC` | Invalid plan type for statement loan |  
| `V5LS4008EC` | Plan and seq number mismatch |  
| `V5LS4008ED` | Plan sequence number not found with plan segment file |  
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
| `V5LF4002EB` | EPP conversion not allowed, account delinquent |
| `V5LF4002EC` | EPP conversion not allowed, invalid account status |
| `V5LF4002ED` | EPP conversion not allowed, account blocked |
| `V5LF4005EA` | APR can not be overridden |
| `V5LF4004EA` | Term is required |
| `V5LF4004EB` | Term is not present in EPP tier table in plan record |
| `V5LF4006EA` | Loan amount is required |
| `V5LF4005EB` | APR can not be overridden |
| `V5LF4002EE` | Maximum plan number reached |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
