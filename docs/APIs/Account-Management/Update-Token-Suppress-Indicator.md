# Update Token Supress Indicator

This service is used to update the token supress Indicator for given account.

## Endpoint

`PUT /v1/accounts/{accountId}/tokenSupressIndicator`

## Payload Example

### Request Payload

```json
{
  "isSupressTokenEnabled": "0"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/tokenSupressIndicator).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `isSupressTokenEnabled` | Payload | *number* | 1 | Token suppression at account level indicator. | 


### Successful Response Payload

```json
{
  "accountId": "0006000011000000137",
  "businessUnit": 600,
  "isSupressTokenEnabled": "0"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000131/tokenSupressIndicator",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
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
| `V5BS0521SN` | Suppress token is not numeric |        
| `V5BS0521SV` | Invalid suppress token | 
| `V5BS0521SZ` | Update access not granted for Suppress Token | 
| `V5BS0010SF` | Update request - Record not found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*