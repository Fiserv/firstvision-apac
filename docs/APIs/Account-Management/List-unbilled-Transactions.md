# List unbilled transactions

This service provides details of the unbilled transactions posted on a given account.

## Endpoint

`GET /v1/accounts/{accountRelationshipNbr}/transactions/cycleToDate`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as and path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountRelationshipNbr}/transactions/cycleToDate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |

### Successful Response Payload

```json
{
  "transactionListRes": [
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052205",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 1,
      "referenceNumber": "FV090921017335430013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052206",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 2,
      "referenceNumber": "FV090921019032730013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052210",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 3,
      "referenceNumber": "FV091321014345330013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052213",
      "creditPlan": 10001,
      "description": "VISA Domestic Restaurant Melbourne    AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 4,
      "referenceNumber": "FV091321017220871972150",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052219",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 5,
      "referenceNumber": "FV091321023074830013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052220",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 6,
      "referenceNumber": "FV091421013262530013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052226",
      "creditPlan": 10001,
      "description": "Dom POS via VISA         SYDNEY       AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 7,
      "referenceNumber": "FV0914210164216L14299",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052227",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "logicModule": 99,
      "postingDate": "17/08/2021",
      "recordNumber": 8,
      "referenceNumber": "FV091421018113030013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052205",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "18/08/2021",
      "logicModule": 99,
      "postingDate": "18/08/2021",
      "recordNumber": 9,
      "referenceNumber": "FV090921017335430013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
    },
    {
      "CardNumber": "0009846801010272888",
      "amount": "$0.00",
      "authorizationCode": "052206",
      "creditPlan": 10001,
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "18/08/2021",
      "logicModule": 99,
      "postingDate": "18/08/2021",
      "recordNumber": 10,
      "referenceNumber": "FV090921019032730013773",
      "transactionCode": 9000,
      "typeOfTransaction": "M"
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
