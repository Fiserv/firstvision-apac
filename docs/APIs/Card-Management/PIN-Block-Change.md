# PIN Block Change

The PIN Block change service is used to update the PIN Block with the prerequisite that the existing PIN block must be supplied and validated.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/cards/{cardNumber}/pinBlockChange`

## Payload Example

### Request Payload

```json
{
  "userFiller": " ",
  "product": 1,
  "signonName": " ",
  "requestedPinBlock": 123456,
  "pinChannel": "A",
  "securitySignon": " ",
  "currentPinBlock": " ",
  "keyAssociation": " ",
  "vgsFiller": " ",
  "pinOffset": 0
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/pinBlockChange).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |
| `currentPinBlock` | Payload | *string* | 16 | Current PIN Block |
| `requestedPinBlock` | Payload | *string* | 16 | PIN block to be updated |

### Successful Response Payload

```json
{
    "cardNumber": "0009543491000080172",
    "userFiller": "",
    "filler": "",
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
