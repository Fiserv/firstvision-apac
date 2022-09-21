# Update Visa Token Status

This service is used to update the token status(Deactivate/Resume/Suspend) of Card.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/tokenStatus`

## Payload Example

### Request Payload

```json
{
  "vtsTokenNumber": "5077400005048482515",
  "status": "1"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/tokenStatus).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 
| `vtsTokenNumber` | Payload | *string* | 19 | Token number assigned by the Visa Tokenization Service(VTS). | 
| `status` | Payload | *string* | 01 | This field indicate the status of token. | 

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010273613",
  "status": "1"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/0009846801010273613/tokenStatus",
    "invalid-params": [
      "V5Z74052EB: TOKEN NBR MUST BE 13 TO 19 DIGITS"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5Z74099SE` | Not signed on to visanet, outgoing requests not possible |
| `V5Z74052EB` | Invalid token details |
| `V5Z74052EA` | Selected token number is spaces or invalid |
| `V5Z74052EB` | Token nbr must be 13 to 19 digits |
| `V5Z74099SE` | Not signed on to visanet, outgoing requests not possible |
| `V5Z74051EA` | Token not received from OFSA |                                   
| `V5Z74051EB` | Please select action code |
| `V5Z74051EC` | Token not found on token master file |
| `V5Z74001IB` | Request accepted successfully |
| `V5Z74013SB` | Account number is invalid |
| `V5Z74099SD` | Not signed on to visanet, outgoing requests not possible |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*