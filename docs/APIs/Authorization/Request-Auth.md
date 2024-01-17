# Request Authorization

This API is used to make an authorization request for payment instrument Id or payment card number.

## Endpoint

`POST /v1/auth/request`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "paymentInstrumentOrCardId": "0009846801010274074",
  "merchantBusinessUnit": 100,
  "merchantId": 999999998,
  "authorizationAmount": "1.00",
  "planId": 10001,
  "expiryDate": 1123,
  "CVV2": 123
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
  "internalReferenceNumber": "3912181393194000",
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "uniqueTransactionId": "APP17977700222011344330001112345678",
  "openToBuy": "$10000.00",
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
    "instance": "/v1/auth/request",
    "invalid-params": [
      "V7RQ4008EA : Expiration date is invalid"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/request).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `merchantBusinessUnit` | Payload | *string* | 3 | Field that identifies the business unit to which the store is assigned. The values for the business unit are 1–998. |
| `merchantId` | Payload | *string* | 9 | Field that identifies the store identification number. |
| `authorizationAmount` | Payload | *string* | 13 | Authorized sales amount in the currency accepted by the particular merchant. |
| `expiryDate` | Payload | *string* | 4 | Valid card expire date should be provided which is of 4 character with MMYY format. |
| `CVV2` | Payload | *string* | 3 | Security code(CVV2/CVC2/CAV2/CVN2) assigned to the payment Instrument id. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V7RQ4001SA` | Auth system record not initialized |
| `V7RQ4001SB` | End-of-day cutoff being processed. |
| `V7RQ4001SC` | After hours update in progress. |
| `V7RQ4001EA` | Request types I K V not allowed for jcb accounts |
| `V7RQ4001EB` | Request types I K V not allowed for off-us uci accounts |  
| `V7RQ4004ED` | Outgoing request not allowed signoff stat=0 |
| `V7RQ4004EB` | Invalid bankcard  not found in bin table |  
| `V7RQ4004EC` | Account number is invalid |
| `V7RQ4004EA` | Check digit issue |
| `V7RQ4004EH` | Request type I or k not available for foreign mc/mc ep accts |
| `V7RQ4099EA/V7RQ4099EB` | Outgoing request not allowed signoff stat 0 |
| `V7RQ4099EC` | Forced authorization requests allowed for on-us accounts only |
| `V7RQ4099ED` | Invalid for prepaid card |
| `V7RQ4099EE` | Credit adjustment requests allowed for on us accounts only |
| `V7RQ4006EA` | Amount must be numeric and greater than zero |
| `V7RQ4002EA` | Merch org is required |  
| `V7RQ4002EB` | Merch nbr is required |  
| `V7RQ4003EA` | Merch status invalid for authorizations |
| `V7RQ4006EB` | Amount must be numeric and greater than zero |
| `V7RQ4007EB` | Credit plan nbr must be values 00001 thru 99998 |
| `V7RQ4008EA` | Expiration date is invalid |
| `V7RQ4011EA` | Address not entered or invalid |
| `V7RQ4013EC` | CVV2 presence indicator and CVV2/cvc2/cvn2/cav2 must be entered |  
| `V7RQ4014EC/V7RQ4014ED` | CVV2/cvc2 is entered the presence ind must be 1 |  
| `V7RQ4006ED` | Amount must be numeric and greater than zero |
| `V7RQ4006EC` | Amount may not contain any decimals |
| `V7RQ4019EA` | Single/dual message ind must be 0 or 1 |
| `V7RQ4002EC` | Merch org must be values 001 thru 998 |
| `V7RQ4098EA` | Local logo record not found |
| `V7RQ4003EB` | Merch record blocked for authorizations |
| `V7RQ4098EA` | Outgoing request not allowed signoff stat 0 |
| `V7RQ4098EB` | Only on-us amex accounts are supported |
| `V7RS0004SF` | FMLG - record not found |
| `V5DC4002SV/V5DC4002SA` | Card number should be numeric and not zeroes |
| `V5DC4004SV` | Valid values are y and n for disable DCVV2 method Flag |
| `V5DC4003SA` | Key association should be greater than spaces |
| `V5DC4001SA` | Invalid card/org |
| `V5DC4001SB` | Org security failed |
| `V5DC4002SB` | Acct is purged/fraud/closed/cgoff or add pending/NOTFND |
| `V5DC4002SC` | Acct is billing/control/diversion acct |
| `V5DC4002SD` | Acct warning code is 1/2/3/4/8 |
| `V5DC4002SE` | Card is add pending/purged/fraud/notfnd |
| `V5DC4002SF` | Card warning code is 1/2/3/4/8 |
| `V5DC4002SG` | Card not active |
| `V5DC4002SH` | Card got expired |
| `V5DC4002SI` | Logo is not found or add pending |
| `V5DC4002SJ` | Not valid visa affiliation |
| `V5DC4002SK` | DCVV2 method is static at logo level |
| `V5DC4002SL` | Hsm call failed |
| `V5DC4002SM` | DCVV2 method is static at global parm level |  
| `V5DC4002SN` | Last generated DCVV2 not expired yet |
| `V5DC4002SO` | Dynamic CVV2 already disabled at card level |  
| `V5DC4002SP` | Dynamic CVV2 already enabled at card level |
| `V5DC4002SQ` | Dynamic CVV2 not enabled at card level |
| `V5DC4002SR` | ZEK pan encryption failed |
| `V5DC4002SS` | ZEK DCVV2 encryption failed |
| `V5DC4002ST` | ZEK card expiry(mm/yy) encryption failed |  
| `V5DC4001SD` | Org is not found at global parm level |
| `V5DC4001IA` | Static CVV2 is set for this card successfully |
| `V5DC4003SB/V5DC4003SE` | Key system file not found |
| `V5DC4003SC/V5DC4003SD` | Key system record read fail |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
