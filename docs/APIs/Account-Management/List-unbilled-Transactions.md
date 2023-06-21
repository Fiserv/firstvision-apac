# List Unbilled Transactions

This API is used to fetch unbilled transaction details for a given account Id.

## Endpoint

`GET /v1/accounts/{accountId}/transactions/cycleToDate`

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
      "authorizationCode": "052205",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV090921017335430013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 1
    },
    {
      "authorizationCode": "052206",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV090921019032730013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 2
    },
    {
      "authorizationCode": "052210",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321014345330013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 3
    },
    {
      "authorizationCode": "052213",
      "description": "VISA Domestic Restaurant Melbourne    AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321017220871972150",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 4
    },
    {
      "authorizationCode": "052219",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091321023074830013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 5
    },
    {
      "authorizationCode": "052220",
      "description": "HOT PIPIS PTY LTD        MOOLOOLABA   AU",
      "effectiveDate": "17/08/2021",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 10001,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "17/08/2021",
      "referenceNumber": "FV091421013262530013773",
      "transactionAmount": "$0.00",
      "transactionCode": 9000,
      "transactionType": "M",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 6
    },
    {
      "authorizationCode": " ",
      "description": " ",
      "effectiveDate": "00/00/0000",
      "merchantCategoryCode": 0,
      "merchantCity": " ",
      "maskedPaymentCardNumber": "000404940XXXXXX4057",
      "planId": 0,
      "paymentInstrumentId": "0009543161012022346",
      "postingDate": "00/00/0000",
      "referenceNumber": " ",
      "transactionAmount": "$0.00",
      "transactionCode": 0,
      "transactionType": " ",
      "uniqueTransactionId": "APP17977700222011344330001112345678",
      "remainingAuthorizationAmount": "$0.00",
      "memoDebitOrCreditIndicator": "D",
      "bnplIplanSequenceNumber": 7
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
    "instance": "/v1/accounts/0001000010000510001/transactions/cycleToDate",
    "invalid-params": [
      "V5T24001EB: NO ORGANIZATION RECORD ON FILE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/transactions/cycleToDate).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5T24001EB` | No organization record on file |
| `V5T24002SB` | Account number not found |
| `V5T24024EA` | Invalid txn suppresion indicatr valid values are N or Y |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
