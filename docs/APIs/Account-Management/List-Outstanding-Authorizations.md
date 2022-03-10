# List Outstanding Authorizations

This service provides details of the memo-posted authorizations on a given account.

## Endpoint

`GET /v1/accounts/{accountRelationshipNbr}/transactions/memoPost`

## Payload Example

### Request Payload

```json

Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.*** 

```  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountRelationshipNbr}/transactions/memoPost).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |

### Successful Response Payload

```json
{
  "aRIndicator": "A",
  "accountNumber": "0000000001000000057",
  "businessUnit": "600",
  "fileFlag": "",
  "fileFlag1": "Y",
  "product": "0",
  "transactionList": [
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    },
    {
      "amount": "$2.00",
      "authorizationCode": " ",
      "creditPlan": "10001",
      "date": "2021260",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "17/09/2021",
      "logicModule": "0",
      "postingDate": "18/08/2021",
      "recordNumber": "0",
      "reference": " ",
      "time": "233208",
      "transactionCode": "0",
      "typeOfTransaction": " "
    }
  ],
  "transactionType": "MEMO POSTED TRANSACTION"
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