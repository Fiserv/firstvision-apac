# PIN Block Change

The PIN Block change service is used to update the PIN Block with the prerequisite that the existing PIN block must be supplied and validated.

## Endpoint

`PUT /v1/cards/{cardNumber}/pinBlockChange`

## Payload Example

### Request Payload

```json
{
  "requestedPinBlock": "123456",
  "currentPinBlock": "2673217",
  "pinOffset": 0,
  "pinChannel": "A",
  "keyAssociation": ""
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/pinBlockChange).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |
| `currentPinBlock` | Payload | *string* | 16 | Code that indicates the original PIN encrypted under a zone PIN key. |
| `requestedPinBlock` | Payload | *string* | 16 | Code that indicates the requested PIN encrypted under a zone PIN key. |
| `pinOffset` | Payload | *number* | 04 | Code that CMS uses to calculate the Personal Identification Number (PIN) for this card. |
| `pinChannel` | Payload | *string* | 01 | Code that indicates the source for reporting purposes. |

### Successful Response Payload

```json
{
  "cardNumber": "0009544410000000047"
}

```

### Error Response Payload

```json
{
  "errorCode": "V5CP4005SZ",
  "errorMessage": "Update access not granted for requested PIN Block"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CP4001SV`| Invalid business unit |  
|`V5CP4006SN`| PIN Offset is not numeric |
|`V5CP4005SZ`| Update access not granted for requested PIN Block |
|`V5CP4006SZ`| Update access not granted for PIN Offset |
|`V5CP4007SZ`| Update access not granted for PIN Channel |
|`V5CP4007SV`| Invalid PIN Channel |
|`V5CP0001SF`| Invalid user |
|`V5CP0021SF`| Not allowed. System in after hours mode |
|`V5CP0022SF`| Not allowed. System in after hours Update mode |
