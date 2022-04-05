# Update Token Supress Indicator

This service is used to update the token supress Indicator for given account. 0 and 1 are valid values. 0 indicates supress token is inactive whereas 1 indicates supress token is active.	

## Endpoint

`PUT /v1/accounts/{accountNumber}/tokenSupressIndicator`

## Payload Example

### Request Payload

```json
{
  "suppressToken": "0"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/tokenSupressIndicator).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique identification number of the account. | 
| `suppressToken` | Payload | *number* | 1 | Token suppression at account level indicator. | 


### Successful Response Payload

```json
{
  "businessUnit": 600,
  "accountNumber": "0006000011000000137",
  "suppressToken": "0"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0521SN",
  "errorMessage": "Suppress token is not numeric"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0521SN` | Suppress token is not numeric |        
| `V5BS0521SV` | Invalid suppress token | 
| `V5BS0521SZ` | Update access not granted for Suppress Token | 
| `V5BS0010SF` | Update Request - Record not found | 

