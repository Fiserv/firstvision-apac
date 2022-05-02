# Update Statement Preference

This API is used to update statement preference for a given account. Some inportant fields like statement reprint flag, statement flag and customer stament flag can be updated with this API.

## Endpoint

`PUT /v1/accounts/{accountNumber}/statementPreference`

## Payload Example

### Request Payload

```json
{
  "statementModeOrStatus": "O",
  "statementReprintAddressFlag": "C",
  "owner/Co-ownerStatementFlag": "0"
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/statementPreference).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the account.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000145",
  "businessUnit": 600,
  "owner/Co-ownerStatementFlag": "0",
  "statementModeOrStatus": "O",
  "statementReprintAddressFlag": "C"
}
```

### Error Response Payload

```json
{
   errorCode" :  V5BS0010SF" ,
   errorMessage" : Update Request - Record not found"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0122SA` | Valid entries are 0 thru 9, H, O, R, S, U, Or Z |