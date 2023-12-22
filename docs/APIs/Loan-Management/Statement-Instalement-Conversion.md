# Statement Balance Conversion

This API is used to convert statement balance into Instalment. API first validates the given plans are eligible for statement balance conversion, if eligible then system converts into instalment for the requested term and also responds with loan scheduling details.

## Endpoint

`POST /v1/loans/statementBalanceConversion`

## Payload Example

<!--
type: tab
-->

```json
{
  "businessUnit": 700,
  "accountId": "0007000011163060009",
  "loanPlanId": 5,
  "annualPercentageRate": "0.0000",
  "tenure": 6,
  "planDetails1": {
    "planId": 1,
    "planSequenceNumber": 1,
    "conversionAmount": "100.00"
  }
}
```

<!--
type: tab
-->

```json
{
    "loanScheduleDetails": [
        {
            "tenure": 0,
            "totalBalance": "$100.00",
            "principalAmount": "$0.00",
            "interestAmount": "$0.10",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 1,
            "totalBalance": "$100.00",
            "principalAmount": "$16.32",
            "interestAmount": "$0.83",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 2,
            "totalBalance": "$83.68",
            "principalAmount": "$16.46",
            "interestAmount": "$0.69",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 3,
            "totalBalance": "$67.23",
            "principalAmount": "$16.59",
            "interestAmount": "$0.56",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 4,
            "totalBalance": "$50.64",
            "principalAmount": "$16.73",
            "interestAmount": "$0.42",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 5,
            "totalBalance": "$33.91",
            "principalAmount": "$16.87",
            "interestAmount": "$0.28",
            "conversionFeeAmount": "$0.00"
        },
        {
            "tenure": 6,
            "totalBalance": "$17.04",
            "principalAmount": "$17.03",
            "interestAmount": "$0.16",
            "conversionFeeAmount": "$0.00"
        }
    ],
    "instalmentDetails": {
        "planIdDescription": "EPP PLAN INTEREST BASED",
        "totalRepaymentAmount": "$102.94",
        "totalInterestAmount": "$2.94",
        "conversionFeeAmount": "$0.00",
        "prorataInterestAmount": "$0.10",
        "instalmentAmount": "$17.15",
        "loanReferenceNumber": "202405300004",
        "totalPrincipalAmount": "$100.00"
    },
    "businessUnit": 700,
    "loanPlanId": 5,
    "accountId": "0007000011163060009",
    "tenure": 7,
    "annualPercentageRate": "10.00000%"
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
      "V5LT4004EA: CONVERSION NOT ALLOWED FOR EXPIRED CARD'S TRANSACTIONS"
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
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `loanPlanId` | Payload  | *integer* | 05 | Identification number of the Credit Plan Master entity.|
| `tenure` | Payload | *integer* | 03 | Field indicates the term used while converting transaction into instalment.|
| `conversionAmount` | Payload | *string* | 17 | Amount requested for instalment conversion..|
| `planId` | Payload | *integer* | 5 | Identification number of the Credit Plan Master entity. The values are 1–99998. You can establish as many as 99,998 Credit Plan Master entity for each organization.|
| `planSequenceNumber` | Payload | *integer* | 3 | Sequence number to identify the entity uniquely.|

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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
