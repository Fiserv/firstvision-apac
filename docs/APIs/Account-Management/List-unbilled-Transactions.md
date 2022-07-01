# List Unbilled Transactions

This service provides details of the unbilled transactions posted on a given account.

## Endpoint

`GET /v1/accounts/{accountId}/transactions/cycleToDate`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/transactions/cycleToDate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Successful Response Payload

```json

{
  "transactionList": [
    {
      "authorizationCode": "052205",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV090921017335430013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052206",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV090921019032730013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052210",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321014345330013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052213",
      "description": "VISA Domestic Restaurant Melbourne    AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321017220871972150",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052219",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321023074830013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052220",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091421013262530013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052226",
      "description": "Dom POS via VISA         SYDNEY       AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV0914210164216L14299",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052227",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091421018113030013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052205",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "18/08/2021",
      "referenceNumber": "FV090921017335430013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    },
    {
      "authorizationCode": "052206",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": "0009846801010272888",
      "planId": 10001,
      "postingDate": "18/08/2021",
      "referenceNumber": "FV090921019032730013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M"
    }
  ]
}
```
### Error Response Payload

```json
{
   errorCode" :  V5T24002SB" ,
   errorMessage" : No account on File"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5T24002SB` | No account on File |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*
