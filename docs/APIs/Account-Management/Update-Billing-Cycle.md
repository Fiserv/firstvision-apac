# Update Billing Cycle
This API is used to update the billing cycle for an account. Business unit and account number can be used to invoke the API. API will validate input request and update the value for requested account.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/accounts/{accountNumber}/billingCycle`

## Payload Example

### Request Payload

```json
{
    "billingCycle": 15
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/billingCycle).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Identification number associated with this Account Base Segment record, the values are 001–998.|
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account.|
| `billingCycle` | payload | *number* | 02 | Cycle code that indicates the day of the month that CMS performs cycle processing for the account. The values are 01–31.|

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000123",
  "billingCycle": 15,
  "businessUnit": 600
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
| `V5BS0121SA` | Valid Entries are 01 Thru 31 |
| `V5BS4001SG` | Org Record not found |