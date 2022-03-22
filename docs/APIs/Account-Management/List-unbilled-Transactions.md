# List unbilled transactions

This service provides details of the unbilled transactions posted on a given account.

## Endpoint

`GET /v1/accounts/{accountRelationshipNbr}/transactions/cycleToDate`

## Payload Example

### Request Payload

> Shoud be empty.
> 
> ***The Business Unit and Account Number should be sent as query parameters and path variable.***



### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountRelationshipNbr}/transactions/cycleToDate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |

### Successful Response Payload

```json
{
  "transactionList": [
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052205",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 1,
      "reference1": "FV090921017335430013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052206",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 2,
      "reference1": "FV090921019032730013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052210",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 3,
      "reference1": "FV091321014345330013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052213",
      "creditPlan1": 10001,
      "description1": "VISA Domestic Restaurant Melbourne    AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 4,
      "reference1": "FV091321017220871972150",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052219",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 5,
      "reference1": "FV091321023074830013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052220",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 6,
      "reference1": "FV091421013262530013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052226",
      "creditPlan1": 10001,
      "description1": "Dom POS via VISA         SYDNEY       AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 7,
      "reference1": "FV0914210164216L14299",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052227",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "17/08/2021",
      "logicModule1": 99,
      "postingDate1": "17/08/2021",
      "recordNumber1": 8,
      "reference1": "FV091421018113030013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052205",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "18/08/2021",
      "logicModule1": 99,
      "postingDate1": "18/08/2021",
      "recordNumber1": 9,
      "reference1": "FV090921017335430013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    },
    {
      "cardNbr": "0009846801010272888",
      "amount1": "$0.00",
      "authorizationCode1": "052206",
      "creditPlan1": 10001,
      "description1": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate1": "18/08/2021",
      "logicModule1": 99,
      "postingDate1": "18/08/2021",
      "recordNumber1": 10,
      "reference1": "FV090921019032730013773",
      "transactionCode1": 9000,
      "typeOfTransaction1": "M"
    }
  ],
  "transactionType": 1
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
