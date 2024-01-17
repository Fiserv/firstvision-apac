# Balance Transfer

This API is used to make an authorization request for payment instrument Id or payment card number when transaction for Balance Transfer.

## Endpoint

`POST /v1/auth/balanceTransfer`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "paymentInstrumentOrCardId": "0009846801010274074",
  "authorizationAmount": "1.00",
  "planId": 10001,
  "transactionDescription": "BT transaction",
  "paymentDate": "20/10/2023",
  "billerCode": "123"
}
```

<!--
type: tab
-->

```json
{
  "responseCode": "00",
  "authorizationCode": "055271",
  "finalAction": "A",
  "reason": "APPROVED",
  "openToBuy": "$10000.00",
  "internalReferenceNumber": "3912181393194000",
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "uniqueTransactionId": "APP17977700222011344330001112345678",
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
    "errorCode": "440401",
    "instance": "/v1/auth/balanceTransfer",
    "invalid-params": [
      "V5CP0004SF : GET REQUEST - RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/balanceTransfer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `authorizationAmount` | Payload | *string* | 17 | Authorized sales amount in the currency accepted by the particular merchant. |
| `planId` | Payload | *integer* | 5 | Plan number that identifies the Credit Plan Master entity associated with the credit plan segment. |
| `transactionDescription` | Payload | *string* | 40 | Transaction source to identify if the authorization is Balance Transfer request. |
| `billerCode` | Payload | *string* | 10 | This field identify the Biller code to which this payment is done. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V7RQ4027EA` | Transaction description is mandatory when tran-type is BP/BT |
| `V7RQ4028EA` | Payment date is mandatory when tran-type is BP/BT |
| `V7RQ4007EC` | Credit plan is mandatory when tran-type is BP/BT |
| `V7RQ4029EA` | Biller code is mandatory when tran-type is BP/BT |
| `V5CP0004SF` | Get Request - Record not found |
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
