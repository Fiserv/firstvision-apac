# Inquire Transaction Instalment Details

This API is used to fetch all the loan details converted from transactions into instalments for a given accountId/paymentInstrumentId.

## Endpoint

`GET /v1/loans/{accountId}/transactionInstalmentDetails`

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
    "transactionInstalmentDetails": [
        {
            "description": "TEST1",
            "authorizationCode": "AAAAAA",
            "effectiveDate": "04/01/2023",
            "postingDate": "05/01/2023",
            "transactionCode": 202,
            "paymentInstrumentId": "0009543161000000609",
            "transactionAmount": "$320.00",
            "referenceNumber": "ABCD001",
            "planId": 5,
            "planSequenceNumber": 1
        },
        {
            "description": "TEST2",
            "authorizationCode": "BBBBBB",
            "effectiveDate": "14/01/2023",
            "postingDate": "15/01/2023",
            "transactionCode": 202,
            "paymentInstrumentId": "0009543161000000609",
            "transactionAmount": "$150.00",
            "referenceNumber": "ABCD002",
            "planId": 5,
            "planSequenceNumber": 1
        }
    ],
    "loanReferenceNumber": "202409300003",
    "accountId": "0007000011000000608",
    "businessUnit": 700,
    "loanStatus": "A",
    "conversionDate": "27/10/2023"
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
    "instance": "/v1/loans/0007000011000000608/transactionInstalmentDetails",
    "invalid-params": [
      "V5LH4002EA: Account / card number is not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/transactionInstalmentDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId path variable. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `loanReferenceNumber` | Query Parameter | *string* | 23 | User-defined identification number for the loan plan.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LH4001EA` | Business unit is not determined |  
| `V5LH4001EB` | Business unit is not present in file |  
| `V5LH4002EA` | Account / card number is not found |
| `V5LH4002EB` | Account / card number is required |
| `V5LH4003EC` | Loan reference number is required |
| `V5LH4003EB` | Invalid loan type |
| `V5LH4003EA` | Loan record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
