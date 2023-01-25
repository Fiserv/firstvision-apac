# List Billed Transactions

This API is used to fetch transaction details a given account Id. Statement date to be provided in input, in order to fetch any specific statement period. If statement date is not given, latest statement details will be fetched.

## Endpoint

`GET /v1/accounts/{accountId}/transactions/lastStatement`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json

{
  "accountId": "0006000011000000137",
  "statementDate": "18/08/2021",
  "transactionList": [
    {
      "authorizationCode": " ",
      "description": "DOMESTIC RETAIL PURCHASE",
      "effectiveDate": "16/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX0137",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "17/08/2021",
      "referenceNumber": "09999999980816000020016",
      "transactionAmount": "$12.00",
      "transactionCode": 4000,
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345678"
    },
    {
      "authorizationCode": " ",
      "description": "DOMESTIC RETAIL PURCHASE",
      "effectiveDate": "16/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX0137",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "17/08/2021",
      "referenceNumber": "09999999980816000020024",
      "transactionAmount": "$8.00",
      "transactionCode": 4000,
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345678"
    },
    {
      "authorizationCode": " ",
      "description": "MEMBERSHIP FEE ASSESSED",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX0137",
      "planId": 10002,
      "paymentInstrumentId": "0009543161000023783",
      "postingDate": "18/08/2021",
      "referenceNumber": "19999999980818199970110",
      "transactionAmount": "$50.00",
      "transactionCode": 7001,
      "transactionType": "D",
      "uniqueTransactionId": "APP17977700222011344330001112345678"
    }
  ]
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
    "instance": "/v1/accounts/0006000011000000131/transactions/lastStatement",
    "invalid-params": [
      "V5S34003SD: ACCOUNT NUMBER NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/transactions/lastStatement).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S34003SD` | Account number not found |
| `V5BS0011SF` | Update Request - Record add pending |
| `V5BS4001EA` | Invalid business unit |
| `V5BS4001SC` | Business unit is in purged status |
| `V5BS4002SA` | Invalid account number |  
| `V5S34003SA` | No statement history information found on file |
| `V5S34222EA` | Invalid txn suppresion indicatr valid values are N or Y |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
