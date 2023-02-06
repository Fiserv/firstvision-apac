# List Outstanding Authorizations

This API is used to fetch outstanding authorization details for a given account Id.

## Endpoint

`GET /v1/accounts/{accountId}/transactions/memoPost`

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
  "transactionList": [
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8266",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$3,000.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
    },
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED DEBIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8221",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
    },
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8211",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
    },
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8243",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
    },
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8296",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
    },
    {
      "authorizationCode": " ",
      "description": "MEMO POSTED CREDIT",
      "effectiveDate": "18/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000444001XXXXXX8211",
      "planId": 10002,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "19/08/2021",
      "referenceNumber": " ",
      "transactionAmount": "$10.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "debitCreditIndicator": "D"
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
    "instance": "/v1/accounts/0006000022000000439/transactions/memoPost",
    "invalid-params": [
      "V5T24002SB: ACCOUNT NUMBER NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/transactions/memoPost).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5T24002SB` | Account number not found |
| `V5T24024EA` | Invalid txn suppresion indicatr valid values are N or Y |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*