# Update Customer's Profile

This service is used to update the various customer profiles like customer number, corresponding customer number and alternate customer details for a given account number.

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.
  
## Endpoint

`PUT /v1/accounts/{accountNumber}/customersProfile`

## Payload Example

### Request Payload

```json
{
  "altCustomerExpiryDate": "15/04/2022",
  "alternateCustomerNumber": "0000000001000000032",
  "alternateCustomerNumberFlag": "A",
  "customerNumber": "9006000000000300015",
  "correspondenceCustomerNumber": "0000000001000000065"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](..api/?type=put&path=/v1/accounts/{accountNumber}/customersProfile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number associated with this Account Base Segment record, the values are 001–998 |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account | 

### Successful Response Payload

```json
{
  "accountNumber": "0004440010000000017",
  "altCustomerExpiryDate": "15/04/2022",
  "alternateCustomerNumber": "0000000001000000032",
  "alternateCustomerNumberFlag": "A",
  "businessUnit": 600,
  "correspondenceCustomerNumber": "0000000001000000065",
  "customerNumber": "9006000000000300015"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0010SF",
  "errorMessage": "Update Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |  
| `V5BS4001SG` | ORG Record Not Found |  
| `V5BS0102SA` | Customer Number Cannot be zeroes |  
| `V5BS0102SB` | Generic Customer Not Allowed |  
| `V5BS0102SC` | No Active Customer On File |    
| `V5BS0172SA` | Generic Customer Not Allowed |  
| `V5BS0172SB` | No Active Customer On File |  
| `V5BS0172SC` | Cust Nbr Not In Add Complete Status |  
| `V5BS0111SA` | Valid Entries Are Space, A, Or B |  
| `V5BS0111SD` | Both Alt Exp Date And Cust Nbr Required |  
| `V5BS0112SA` | Alt Cust Expires Date Should Be A Future Date |  