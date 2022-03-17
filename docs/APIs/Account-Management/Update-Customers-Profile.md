# Update Customer's Profile... TEST

This service is used to update the various customer profiles like customer number, corresponding customer number and alternate customer details for a given account number.
  
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
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the account | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

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
| `V5BS4001SG` | Org record not found |  
| `V5BS0102SA` | Customer number cannot be zeroes |   
| `V5BS0102SC/V5BS0172SB` | No active customer on file |    
| `V5BS0172SA/V5BS0102SB` | Generic customer not allowed |  
| `V5BS0172SC` | Cust number not in add complete status |  
| `V5BS0111SA` | Valid entries are space, A, or B |  
| `V5BS0111SD` | Both alt exp date and cust number required |  
| `V5BS0112SA` | Alt cust expires date should be a future date |  
