# Change PIN

The PIN Block change service is used to update the PIN Block with the prerequisite that the existing PIN block must be supplied and validated.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/pinBlockChange`

## Payload Example

### Request Payload

```json
{
  "requestedPinBlock": "123456",
  "currentPinBlock": "2673217",
  "pinOffset": 0,
  "pinChannel": "A",
  "keyAssociation": " "
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/pinBlockChange).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `currentPinBlock` | Payload | *string* | 16 | Code that indicates the original PIN encrypted under a zone PIN key. |
| `requestedPinBlock` | Payload | *string* | 16 | Code that indicates the requested PIN encrypted under a zone PIN key. |
| `pinOffset` | Payload | *number* | 04 | Code that CMS uses to calculate the Personal Identification Number (PIN) for this card. |
| `pinChannel` | Payload | *string* | 01 | Code that indicates the source for reporting purposes. |

### Successful Response Payload

```json
{
}

```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/0009544410000000041/pinBlockChange",
    "invalid-params": [
      "V5CP4003SA: INVALID ACCOUNT TYPE, PIN CHANGE NOT ALLOWED"
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
|`V5CP4001SA`| Organization record not found | 
|`V5CP4002SA`| Invalid account status, pin change not allowed | 
|`V5CP4003SA`| Invalid account type, pin change not allowed | 
|`V5CP4004SA`| Account blocked, pin change not allowed | 
|`V5CP4005SA`| Account does not have active cards | 
|`V5CP4006SA`| Invalid card status, pin change not allowed | 
|`V5CP4007SA`| Card blocked, pin change not allowed | 
|`V5CP4008SA`| PIN change not allowed for smart cards through web or IVR | 
|`V5CP4009SA`| Card is not activated, pin change not allowed | 
|`V5CP4010SA`| PIN suppression is on, pin change not allowed | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
