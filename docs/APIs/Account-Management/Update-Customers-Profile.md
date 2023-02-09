# Update Customers' Profile

This service is used to update the various customer profiles like customer id, corresponding customer id and alternate customer details for a given account id.
  
## Endpoint

`PUT /v1/accounts/{accountId}/customersProfile`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "customerId": "0000000001000000032",
  "correspondenceCustomerId": "0000000001000000065",
  "alternateCustomerIdDetails": {
    "customerIdFlag": "A",
    "customerId": "0000000001000000065",
    "customerIdExpiryDate": "15/04/2022",
    "customerIdEffectiveDate": "14/01/2021"
  }
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0004440010000000017",
  "alternateCustomerIdDetails": {
    "customerId": "0000000001000000065",
    "customerIdEffectiveDate": "14/01/2021",
    "customerIdExpiryDate": "15/04/2022",
    "customerIdFlag": "A"
  },
  "businessUnit": 600,
  "correspondenceCustomerId": "0000000001000000065",
  "customerId": "0000000001000000032"
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0004440010000000017/customersProfile",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/customersProfile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |  
| `V5BS4001SG` | Org record not found |  
| `V5BS0102SA` | Customer number cannot be zeroes |   
| `V5BS0102SC/V5BS0172SB` | No active customer on file |    
| `V5BS0172SA/V5BS0102SB` | Generic customer not allowed |  
| `V5BS0172SC` | Cust number not in add complete status |  
| `V5BS0111SA` | Valid entries are space, A, or B |  
| `V5BS0111SD` | Both alt exp date and cust number required |  
| `V5BS0112SA` | Alt cust expires date should be a future date |  

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
