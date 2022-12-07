# List Transactions by Date Range

This service provides the list of various transactions like memo, outstanding, unbilled and billed with in a given a date range. 

## Endpoint

`GET /v1/accounts/{accountId}/listTransactions`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id, start/end date should be sent as path variable and query parameter.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/listTransactions).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `startDate` | Query Parameter | *date* | 10 | Start date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. | 
| `endDate` | Query Parameter | *date* | 10 | End date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |

### Successful Response Payload

```json

{
  "transactionList": [
    {
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "20210513",
      "maskedPaymentCardNumber": "",
      "merchantCity": "",
      "merchantCategoryCode": 50367,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "VT211330002000010000025",
      "transactionAmount": "1000",
      "transactionCode": 4000,
      "transactionType": "D",
      "transactionIndicator": "P"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "maskedPaymentCardNumber": "",
      "merchantCity": "",
      "merchantCategoryCode": 50367,
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980040",
      "transactionAmount": "400",
      "transactionCode": 7016,
      "transactionType": "C",
      "transactionIndicator": "P"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210525",
      "maskedPaymentCardNumber": "",
      "merchantCity": "",
      "merchantCategoryCode": 50367,
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210525",
      "referenceNumber": "19999999980525199980020",
      "transactionAmount": "500",
      "transactionCode": 7016,
      "transactionType": "C",
      "transactionIndicator": "P"
    }
  ]
}

```
### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000131/listTransactions",
    "invalid-params": [
      "V5TD4001IA: No transactions found for request"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5TD4001IA` | No transactions found for request |
| `V5TD4004EA` | Account number not numeric or euqal to spaces |
| `V5TD4003EA` | Org must be numeric and valid values are 001-998 |
| `V5TD4008EA` | Number of transactions not numeric or greater than 50 |
| `V5TD4005EA` | Invalid local/foreign indicator valid values are space 'l' or 'F' |
| `V5TD4006EA` | Transaction detail begin date/date from is not numeric/zeroes |
| `V5TD4007EA` | Transaction detail end date/date to is not numeric/zeroes/9999999 |
| `V5TD4006EB` | Transaction End date must be greater than transaction begin date |
| `V5TD4006EC` | Transaction detail begin date/date from format is invalid |
| `V5TD4006ED` | Transaction detail begin date/date from is not numeric/zeroes |
| `V5TD4007EB` | Transaction detail end date/date to format is invalid |
| `V5TD4007EC` | Transaction detail end date/date to is not numeric/zeroes/9999999 |
| `V5TD4003SD` | Organization number not found on file |



*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
