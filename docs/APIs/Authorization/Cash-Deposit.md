# Cash Deposit

This API is used to perform cash deposit transactions for a given payment instrument id or payment card number. 

## Endpoint

`POST /v1/auth/cashDeposit`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "authorizationAmount": "120.00",
  "merchantBusinessUnit": 100,
  "paymentInstrumentOrCardId": "0009846801010274074",
  "referenceNumber": "12345667888888888454765",
  "channelId": "BQIB",
  "transactionDescription": "Cash Deposit",
  "transactionType": "CP",
  "branchNumber": 234654
}
```

<!--
type: tab
-->

```json
{
  "authorizationCode": "055271",
  "cashAvailable": "$1000.00",
  "effectiveDate": "10/01/2022",
  "finalAction": "A",
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "openToBuy": "$10000.00",
  "reason": "APPROVED",
  "referenceNumber": "12345667888888888454765",
  "responseCode": "00",
  "uniqueTransactionId": "APP17977700222011344330001112345678"
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
    "instance": "/v1/auth/cashDeposit",
    "invalid-params": [
      "V7RQ4004EB : INVALID BANKCARD  NOT FOUND IN BIN TABLE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/cashDeposit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `authorizationAmount` | Payload | *string* | 13 | Authorized sales amount in the currency accepted by the particular merchant. |
| `transactionType` | Payload | *string* | 2 | Field to identify the type of transaction. |
| `channelId` | Payload | *string* | 4 | Field indicate the partner details and transaction source. |
| `referenceNumber` | Payload | *string* | 23 | Reference number assigned to the transaction to identify the transaction uniquely. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V7RQ4004EB` | Invalid bankcard  not found in bin table |  
| `V7RQ4004EC` | Account number is invalid |
| `V7RQ4004EA` | Check digit issue |
| `V7RQ4001SC` | After hours update in progress. |
| `V7RQ4003EA` | Merch status invalid for authorizations |
| `V7RQ4007EB` | Credit plan nbr must be values 00001 thru 99998 |
| `V7RQ4006ED` | Amount must be numeric and greater than zero |
| `V7RQ4002EC` | Merch org must be values 001 thru 998 |
| `V7RQ4003EB` | Merch record blocked for authorizations |
| `V5DC4002SV/V5DC4002SA` | Card number should be numeric and not zeroes |
| `V5DC4001SA` | Invalid card/org |
| `V5DC4001SB` | Org security failed |
| `V5DC4002SB` | Acct is purged/fraud/closed/cgoff or add pending/NOTFND |
| `V5DC4002SD` | Acct warning code is 1/2/3/4/8 |
| `V5RQ4030SB` | Settlement date should be greater than auth date |
| `V7RQ4026SV` | Valid values for tran type are spaces, BT, BP, TC, PA, DP, CP |
| `V7RQ4031EA` | Channel id is mandatory when tran-type is TC/PA/DP/CP |
| `V7RQ4033EA` | Branch nbr is mandatory for txn done at branch |
| `V7RQ4032EA` | Reference nbr is mandatory when tran-type is TC/PA/DP/CP |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*