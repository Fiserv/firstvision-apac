# Board Customer

This API is used to create a new customer record. This record will have demographic information of customer.

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/customers/boardCustomer`

## Payload Example

### Request Payload

```json
{
  "businessUnit": 600,
  "productId": 2,
  "dualFlag": 0,
  "title": "Mr",
  "nameTypeIndicator1": "0",
  "nameTypeIndicator2": "0",
  "nameTypeIndicator3": "0",
  "residentialFlag": "1",
  "homePhone": "11230342",
  "employeePhone": "67894",
  "birthDate": "01/02/2010",
  "externalId": "2363-12-2839-1",
  "gender": "1",
  "emailAddress": "abc@goole.com",
  "alternateEmailAddress": "abc1@google.com",
  "mobileNumber": "11231232",
  "emailAddressFlag": "1",
  "addressDataReq": {
    "addressLine3": "CHITRAPURI",
    "addressLine4": "DELHI",
    "addressLine1": "FLAT NO:404",
    "addressLine2": "RAINBOW APTS",
    "city": "DELHI",
    "stateProvince": "DL",
    "countryCode": "IND",
    "postalCode": "110004"
  },
  "namesDataReq": {
    "birthName": "",
    "givenName": "ABC",
    "middleName": "",
    "nameLine1": "M S SWAMY",
    "nameLine2": "KK",
    "nameLine3": " "
  }
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/boardCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 3 | Unique identification number associated with the organization. Valid values from 001-998. |
| `productId` | Payload | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 001-998. |
| `firstName` | Payload | *string* | 40 | First name of customer. |

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "customerId": "0006000012000000768"
}
```

### Error Response Payload

```json
{
   "errorCode" :  "V5SB4003EA" ,
   "errorMessage" : "Base account number is required"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record incomplete | 
| `V5SB4154SA` | Customer number not on file for this org |
| `V5SB4154SB` | Customer number already exists for this org | 
| `V5SB4154SD` | Generic Customer not allowed |
| `V5SB4155EA` | Customer number not on file for the dual org | 
| `V5SB4155EB` | Generic Customer not allowed |
| `V5SB4155EC` | Customer number already exists for the dual org |
| `V5SB4154EA` | Invalid Customer number | 
| `V5SB4160EE` | Invalid Customer check digit for this org |                         
| `V5SB4160EG` | Invalid Customer check digit for dual org |
| `V5NA4081EA` | First name is required |