# Update Statement Preference

This API is used to update statement preference for a given account. This API can be be invoked with an business unit and account number.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/accounts/{accountNumber}/statementPreference`

## Payload Example

### Request Payload

```json
{
  "statementReprintFlag": "C",
  "statementFlag": "O",
  "customerStatementFlag": 0
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/statementPreference).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter| *number* | 03 | Identification number associated with this Account Base Segment record, the values are 001–998.|
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account.|

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000123",
  "businessUnit": 600,
  "customerStatementFlag": "0",
  "statementFlag": "O",
  "statementReprintFlag": "C"
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
| `V5BS0122SA` | valid Entries Are 0 Thru 9, H, O, R, S, U, Or Z |