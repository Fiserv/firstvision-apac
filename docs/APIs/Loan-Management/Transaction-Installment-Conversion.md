# Transaction Instalment Conversion

This API supports both single and multiple transaction conversion into instalments. API first validates if given transactions are eligible to convert into instalment. If transactions are eligible, then system converts given transactions into instalment.

## Endpoint

`POST /v1/loans/transactionConversion`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
    "businessUnit": 700,
    "accountId": "0007000011888095801",
    "loanPlanId": 8,
    "annualPercentageRate": "0.0000",
    "tenure": 6,
    "transactionDetails1": {
        "transactionAmount": "450.00",
        "effectiveDate": "10/12/2023",
        "referenceNumber": "123456781",
        "authorizationCode": "123457"
    },
    "transactionDetails2": {
        "transactionAmount": "450.00",
        "effectiveDate": "11/12/2023",
        "referenceNumber": "123456789",
        "authorizationCode": "123456"
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
            "interestAmount": "$0.00",
            "tenure": 0,
            "totalBalance": "$900.00",
            "principalAmount": "$0.00",
            "conversionFeeAmount": "$0.90"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 1,
            "totalBalance": "$900.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 2,
            "totalBalance": "$750.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 3,
            "totalBalance": "$600.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 4,
            "totalBalance": "$450.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 5,
            "totalBalance": "$300.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        },
        {
            "interestAmount": "$0.00",
            "tenure": 6,
            "totalBalance": "$150.00",
            "principalAmount": "$150.00",
            "conversionFeeAmount": "$0.00"
        }
    ],
    "instalmentDetails": {
        "loanReferenceNumber": "202405300004",
        "totalRepaymentAmount": "$900.00",
        "prorataInterestAmount": "$0.00",
        "instalmentAmount": "$150.00",
        "conversionFeeAmount": "$0.90",
        "planIdDescription": "TIP EPP PLAN FEE BASED",
        "totalInterestAmount": "$0.00",
        "totalPrincipalAmount": "$900.00"
    },
    "businessUnit": 700,
    "loanPlanId": 8,
    "accountId": "0007000011888095801",
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
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/loans/transactionConversion",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/loans/transactionConversion).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `loanPlanId` | Payload  | *integer* | 05 | Identification number of the Credit Plan Master entity.|
| `tenure` | Payload | *integer* | 03 | Field indicates the term used while converting transaction into instalment.|
| `transactionAmount` | Payload | *string* | 17 | Amount of the transaction.|
| `effectiveDate` | Payload | *string* | 10 | Effective date of the transaction, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control.|
| `referenceNumber` | Payload | *string* | 23 | Reference number assigned to the transaction.|
| `authorizationCode` | Payload | *string* | 06 | Authorization code assigned to the transaction.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LT4002EB` | Business unit is not valid |  
| `V5LT4002EC` | EPP inactive, conversion not allowed |  
| `V5LT4001ED` | Account number not found |
| `V5LT4003EA` | Mutlti TIP is not active for promo plan |
| `V5LT4004EA` | Conversion not allowed for expired card's transactions |
| `V5LT4004EB` | Conversion not allowed for billed transactions |  
| `V5LT4004EC` | Transaction amount is not within range of EPP amount limit |  
| `V5LT4005SA` | Conversion not allowed for disputed transctions |
| `V5LT4006SA` | Conversion not allowed for cancelled transactions |
| `V5LT4007SA` | Transaction is already converted |
| `V5LT4008SA` | Cumulative transaction amt is not within rage of epp max limit |
| `V5LT4009EA` | Transaction amt/date not matching with input |
| `V5LT4010EA` | Transaction record is not present in AMOS |
| `V5LT4011EA` | AMOS read failed for conversion |
| `V5LT4011EB` | AMOS update failed for conversion |
| `V5LT4064EA` | AMPS plan write - duplicate record found |
| `V5LT4066EA` | AMLS write - duplicate record found |
| `V5LT4065EA` | AMPS loan write - duplicate record found |
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
