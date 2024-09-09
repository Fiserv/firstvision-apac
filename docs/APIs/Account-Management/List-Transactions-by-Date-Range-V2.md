# List Transactions by Date Range V2

This API is used to fetch the list of various transactions like authorizations, memos, outstanding authorizations, unbilled and billed transactions for a given date range and account Id/paymentInstrumentId.

## Endpoint

`POST /v2/accounts/listTransactions`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 200,
  "accountId": "0002000010000066752",
  "startDate": "01/06/2020",
  "endDate": "30/06/2021",
  "isTransactionSuppressionEnabled": "N",
  "transactionIndicator": "P",
  "additionalCardDetails": {
    "paymentInstrumentId1": "0002000010000066752",
    "paymentInstrumentId2": "0002000010000066751",
    "paymentInstrumentId3": "0002000010000066753",
    "paymentInstrumentId4": "0002000010000066754",
    "paymentInstrumentId5": "0002000010000066755"
  },
  "continuationToken": " "
}
```

<!--
type: tab
-->

```json

{
  "transactionList": [
    {
      "authorizationCode": "021447",
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "20210513",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": "COLES",
      "merchantCategoryCode": 32303,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "VT211330002000010000025",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$1000.00",
      "transactionCode": 4000,
      "transactionIndicator": "S",
      "transactionType": "D",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000001",
			"transactionIdentifier": "699999261226140",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": "021447",
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "20210513",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": "COLES",
      "merchantCategoryCode": 32303,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "VT211330002000010000026",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$100.00",
      "transactionCode": 4579,
      "transactionIndicator": "S",
      "transactionType": "D",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000011",
			"transactionIdentifier": "699999261226141",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": " ",
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210513",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": "COLES",
      "merchantCategoryCode": 32303,
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "19999999980513199980010",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$1000.00",
      "transactionCode": 7016,
      "transactionIndicator": "S",
      "transactionType": "C",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000002",
			"transactionIdentifier": "699999261226142",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": "022709",
      "description": "Wall Mart LLC AUS      Sydney        AU",
      "effectiveDate": "20210518",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": "COLES",
      "merchantCategoryCode": 32303,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210518",
      "referenceNumber": "VT211380004000010000001",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$1501.00",
      "transactionCode": 4567,
      "transactionIndicator": "S",
      "transactionType": "C",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000003",
			"transactionIdentifier": "699999261226143",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": " ",
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210518",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": " ",
      "merchantCategoryCode": 0,
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210518",
      "referenceNumber": "19999999980518199980010",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$1501.00",
      "transactionCode": 7015,
      "transactionIndicator": "S",
      "transactionType": "D",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000004",
			"transactionIdentifier": "699999261226144",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": "023754",
      "description": "Wall Mart LLC          Sydney        AU",
      "effectiveDate": "20210519",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": " ",
      "merchantCategoryCode": 0,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000010",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$1111.00",
      "transactionCode": 4000,
      "transactionIndicator": "S",
      "transactionType": "D",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000015",
			"transactionIdentifier": "699999261226145",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": "023911",
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": " ",
      "merchantCategoryCode": 0,
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000064",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$2500.00",
      "transactionCode": 6800,
      "transactionIndicator": "S",
      "transactionType": "D",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000005",
			"transactionIdentifier": "699999261226146",
			"multiClearSequenceIndicator": "0"
    },
    {
      "authorizationCode": " ",
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210525",
      "maskedPaymentCardNumber": " ",
      "merchantCity": " ",
      "merchantName": " ",
      "merchantCategoryCode": 0,
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210525",
      "referenceNumber": "19999999980525199980020",
      "remainingAuthorizationAmount": "$0.00",
      "transactionAmount": "$500.00",
      "transactionCode": 7016,
      "transactionIndicator": "S",
      "transactionType": "C",
      "uniqueTransactionId": " ",
      "memoDebitOrCreditIndicator": "D",
      "merchantCountryCode": "AUS",
      "upiMerchantId": "102345679321431",
      "billerCode": " ",
      "foreignOriginalAmount": "0",
      "foreignOriginalCurrencyCode": "000",
      "acquirerReferenceNumber": "74126780192471000000006",
			"transactionIdentifier": "699999261226147",
			"multiClearSequenceIndicator": "0"
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
    "instance": "/v2/accounts/listTransactions",
    "invalid-params": [
      "V5TD4004EB: ACCOUNT NUMBER NOT FOUND/ADD PENDING/CLOSED/PURGED"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v2/accounts/listTransactions).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId in request. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `startDate` | Payload | *date* | 10 | Start date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |
| `endDate` | Payload | *date* | 10 | End date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5TD4001IA` | No transactions found for request |
| `V5TD4004EA` | Account number not numeric or euqal to spaces |
| `V5TD4004EB` | Account number not found/add pending/closed/purged |
| `V5TD4003EA` | Org must be numeric and valid values are 1-998 |
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
| `V5TD4016EB` | Card number is not associated with provided account number |
| `V5TD4016EA` | Embosser record not on card file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
