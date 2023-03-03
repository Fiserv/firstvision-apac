# Inquire Authorization Details

This API is used to fetch Authorization details for a given payment instrument Id or payment card number, authorization code, effective date, and transaction amount, if given. This API fetches data for any authorization which is waiting for settlement.

## Endpoint

`GET /v1/auth/{paymentInstrumentOrCardId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Payment Instrument Or Card Id and effective date, authorization code should be sent as path variable and query parameter.***

<!--
type: tab
-->

```json
{
  "accountDetails": {
    "accountOpenDate": "01/05/2021",
    "cardFeeDate": "00/00/0000",
    "chargeOffDate": "00/00/0000",
    "chargeOffReason": "",
    "chargeOffStatus": "0",
    "creditClassification": "N1",
    "creditLimitOverlimitPercentage": "$1.00",
    "customerid": "0001000000000150191",
    "delinquentPaymentDaysCount": "000",
    "lastDelinquentDate": "00/00/0000",
    "lastPaymentAmount": "$0.00",
    "lastPaymentDate": "00/00/0000",
    "lastPurchaseAmount": "$0.00",
    "lastPurchaseDate": "00/00/0000",
    "lastReturnCheckCount": 0,
    "lastReturnCheckDate": "00/00/0000",
    "lastStatementDate": "30/04/2021"
  },
  "accountStatus": "A",
  "action": "A",
  "authorizationCode": "055358",
  "availableCredit": "$8,946.36",
  "blockAndWarningCodeDetails": {
    "blockCode1": "",
    "blockCode1Date": "00/00/0000",
    "blockCode2": "",
    "blockCode2Date": "00/00/0000",
    "warningCode": "0000000"
  },
  "collectionDetails": {
    "collectionDate": "00/00/0000",
    "collectionReason": 0
  },
  "creditLimit": "$0.00",
  "currentBalance": "$0.00",
  "currentCycleDue": 0,
  "delinquentDaysCount": 0,
  "disputedAmount": "$0.00",
  "disputedItemCount": 0,
  "expiryDate": "30/04/2024",
  "maskedPaymentCardNumber": "000404940XXXXXX5286",
  "uniqueTransactionId": "APP17977700222011344330001112345678",
  "memoDetails": {
    "memoCreditAmount": "$0.00",
    "memoCreditCount": 0,
    "memoDebitAmount": "$549.58",
    "memoDebitCount": 134
  },
  "merchantDetails": {
    "merchantBusinessUnit": 100,
    "merchantCategoryCode": "05999",
    "merchantId": "999999998"
  },
  "planId": "10001",
  "reason": "APPROVED",
  "responseCode": "00",
  "temporaryCreditLimit": "$0.00",
  "totalDueAmount": "$0.00",
  "transactionAmount": "2.00",
  "effectiveDate": "10/01/2022"
}
```

<!--
type: tab
-->

```json

[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/auth/0009846801010274074/details",
    "invalid-params": [
      "V7RS4003EQ : Input effective date not matching with log record effective date "
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/auth/{paymentInstrumentOrCardId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `effectiveDate` | Query vari | *string* | 10 | Effective Date of the transaction. The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |
| `authorizationCode` | Payload | *string* | 6 | Authorization code associated with the transaction. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V7RS4002EP` | Invalid card number |
| `V7RS4002ES` | Authorization record not found |
| `V7RS4003EQ` | Input effective date not matching with log record effective date |
| `V7RS4005ER` | Input auth amount not matching with log record auth amount |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
