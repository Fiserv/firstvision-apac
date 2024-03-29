# Change PIN

This API is used to update the PIN Block with the prerequisite that the existing PIN block must be supplied and validated before the new PIN block is replaced. This API could be triggered from the ATM or other digital channels such as online (WEB) or mobile banking.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/pinBlockChange`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "requestedPinBlock": "0B84D9726EF0F480",
  "currentPinBlock": "B2AFACDD4874EC07",
  "pinOffset": 0,
  "pinChannel": "A",
  "keyAssociation": " ",
  "pinChangeActionCode": "PNRS",
  "pinChangeMemo": "Set PIN"
}
```

<!--
type: tab
-->

```json
{
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
    "instance": "/v1/cards/0009544410000000041/pinBlockChange",
    "invalid-params": [
      "V5CP4003SA: ACCOUNT NUMBER NOT FOUND, PIN CHANGE NOT ALLOWED"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/pinBlockChange).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `requestedPinBlock` | Payload | *string* | 16 | Code that indicates the requested PIN encrypted under a zone PIN key. |
| `pinChannel` | Payload | *string* | 01 | Code that indicates the source for reporting purposes. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CP4001SA`| Organization record not found |
|`V5CP4002SA`| Invalid account status, pin change not allowed |
|`V5CP4003SA`| Account number not found, pin change not allowed |
|`V5CP4004SA`| Account blocked, pin change not allowed |
|`V5CP4005SA`| Account does not have active cards |
|`V5CP4006SA`| Invalid card status, pin change not allowed |
|`V5CP4007SA`| Card blocked, pin change not allowed |
|`V5CP4008SA`| PIN change not allowed for smart cards through web or IVR |
|`V5CP4009SA`| Card is not activated, pin change not allowed |
|`V5CP4010SA`| PIN suppression is on, pin change not allowed |
|`V5CP4009EB`| Invalid PIN set/reset action code |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
