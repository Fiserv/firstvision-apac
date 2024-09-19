# PayAll

This API is used process pay all transactions for a given payment instrument Id or payment card number.

## Endpoint

`POST /v1/auth/payAll`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "authorizationAmount": "100.00",
  "channelId": "PALL",
  "merchantBusinessUnit": 100,
  "merchantCategoryCode": 0,
  "paymentInstrumentOrCardId": "0009846801010274074",
  "planId": 10001,
  "settlementDate": "10/01/2022",
  "transactionDescription": "Bill payment transaction",
  "transactionType": "NA",
  "uniqueTransactionId": "APP17977700222011344330001112345678"
}
```

<!--
type: tab
-->

```json
{
  "authorizationCode": "055271",
  "effectiveDate": "10/01/2022",
  "finalAction": "A",
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "openToBuy": "$10020.00",
  "reason": "APPROVED",
  "responseCode": "00",
  "settlementDate": "10/01/2022",
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
    "errorCode": "440402",
    "instance": "/v1/auth/payAll",
    "invalid-params": [
      "V7RQ4004EC : ACCOUNT NUMBER IS INVALID"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/payAll).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `authorizationAmount` | Payload | *string* | 13 | Authorized sales amount in the currency accepted by the particular merchant. |
| `transactionType` | Payload | *string* | 2 | Field to identify the type of transaction. |
| `transactionDescription` | Payload | *string* | 40 | Transaction source to identify if the authorization is for BPAY OUT request. |
| `merchantCategoryCode` | Payload | *number* | 4 | Merchant category code. |

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
| `V7RQ4026SV` | Valid values for tran type are spaces, BT, BP, TC, PA, DP, CP, NA & OF |
| `V7RQ4024EA` | MCC is mandatory for payall txn |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
