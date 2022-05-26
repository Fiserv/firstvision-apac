# List Outstanding Authorizations

This service provides details of the memo-posted authorizations on a given account.

## Endpoint

`GET /v1/accounts/{accountId}/transactions/memoPost`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/transactions/memoPost).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Successful Response Payload

```json

{
  "transactionListRes": [
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$3,000.00",
      "transactionCode": 0,
      "transactionType": " "
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " "
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " "
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " "
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " "
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "paymentInstrumentId": " ",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " "
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