# Request Authorization 

This service is used for Authorization request on payment instrument id.

## Endpoint

`POST /v1/auth/authRequest`

## Payload Example

### Request Payload

```json
{
  "paymentInstrumentOrCardId": "0009846801010274074",
  "merchantBusinessUnit": 100,
  "merchantId": 999999998,
  "authorizationAmount": 1,
  "planId": 10001,
  "expiryDate": 1123,
  "CVV2": 123
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/authRequest).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `merchantBusinessUnit` | Payload | *string* | 3 | Field that identifies the business unit to which the store is assigned. The values for the business unit are 001–998. |
| `merchantId` | Payload | *string* | 9 | Field that identifies the store identification number. |
| `authorizationAmount` | Payload | *number* | 17 | Authorized sales amount in the currency accepted by the particular merchant. |
| `expiryDate` | Payload | *string* | 4 | Valid card expire date should be provided which is of 4 character with MMYY format. |
| `CVV2` | Payload | *string* | 3 | Security code(CVV2/CVC2/CAV2/CVN2) assigned to the payment Instrument id. |

### Successful Response Payload

```json
{
  "responseCode": 0,
  "authorizationCode": "055271",
  "finalAction": "A",
  "reason": "APPROVED",
  "internalReferenceNumber": 3239000,
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "uniqueTransactionId": "APP179777002220113443300011123456789"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/auth/authRequest",
    "invalid-params": [
      "V7RQ4008EA : Expiration date is invalid"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V7RQ4001SA` | Auth system record not initialized |
|`V7RQ4001SB` | End-of-day cutoff being processed | 
|`V7RQ4001SC` | After hours update in progress |
|`V7RQ4001EE` | Country code not valid in cms org rec for merch |
|`V7RQ4002EA` | Merch org is required |                                             
|`V7RQ4002EC` | Merch org must be values 001 thru 998 | 
|`V7RQ4003EA` | Merch status invalid for authorizations |
|`V7RQ4003EB` | Merch record blocked for authorizations | 
|`V7RQ4004EB` | Invalid bankcard not found in bin table |                          
|`V7RQ4004EA` | Check digit issue |                                                 
|`V7RQ4006EA` | Amount must be numeric and greater than zero |
|`V7RQ4006EC` | Amount may not contain any decimals | 
|`V7RQ4007EA` | Credit plan nbr is required |
|`V7RQ4007EB` | Credit plan nbr must be values 00001 thru 99998 | 
|`V7RQ4008EA` | Expiration date is invalid |
|`V7RQ4013EC` | CVV2 presence indicator and CVV2/CVC2/CVN2/CAV2 must be entered | 
|`V7RQ4014EC` | CVV2/CVC2 is entered the presence ind must be 1 |   

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*