# Reverse Authorization 

This service is used for Authorization reversal on payment instrument id.

## Endpoint

`POST /v1/auth/reverse`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentOrCardId": "0009846801010274074",
  "effectiveDate": "20/11/2022",
  "authorizationCode": "055271",
  "authorizationAmount": "$100.00"
}

```

<!--
type: tab
-->

```json
{
  "responseCode": 0,
  "authorizationCode": "055271",
  "finalAction": "R",
  "reason": "REVESAL",
  "internalReferenceNumber": 3239000,
  "uniqueTransactionId": "APP179777002220113443300011123456789",
  "maskedPaymentCardNumber": "000484680XXXXXX9405",
  "openToBuy": "$10000.00"
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
    "instance": "/v1/auth/reverse",
    "invalid-params": [
      "V7RS4002ES: AUTHORIZATION RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/auth/reverse).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentOrCardId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `effectiveDate` | Payload | *string* | 10 | Effective Date of the transaction. The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |
| `authorizationCode` | Payload | *string* | 6 | Authorization code associated with the transaction. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V7RS4002EP` | Invalid card number |        
| `V7RS4003EQ` | Input effective date not matching with log record effective date |   
| `V7RS4005ER` | Input auth amount not matching with log record auth amount |   
| `V7RS4002ES` | Authorization record not found |   
| `V7RS4002EK` | Transaction is already reversed |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*