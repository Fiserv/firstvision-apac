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
  "product": 2,
  "dualFlag": 0,
  "title": "ADWSQQ",
  "nameTypeIndicator1": "0",
  "nameTypeIndicator2": "0",
  "nameTypeIndicator3": "0",
  "nameLine1": "John",
  "nameLine2": "Jacob ",
  "nameLine3": "Samuel",
  "addressLine1": "House No. 12",
  "addressLine2": "S.H. Qo",
  "addressLine3": "California",
  "addressLine4": "USA",
  "city": "La Vegas",
  "state": "CL",
  "postalCode": "112345",
  "countryCode": "USA",
  "residentialFlag": "1",
  "homePhone": "11230342",
  "employeePhone": "67894",
  "dateOfBirth": "01/02/2010",
  "lastName": "Christopher",
  "middleName": "",
  "firstName": "Samuel",
  "nationalID": "2363-12-2839-1",
  "gender": "1",
  "email": "abc@goole.com",
  "alternateEmail": "abc1@google.com",
  "mobileNumber": "11231232",
  "emailFlag": "1"
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/boardCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |
| `firstName` | Payload | *string* | 40 | First name of customer. |

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "customerNumber": "0006000012000000543"
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
| `V5SB4003EA` | Base account number is required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number is required |
| `V5SB4005EA` | Customer NA account must be blank | 
| `V5SB4005EB` | Customer NA account required |
| `V5SB4005EG` | Customer NA account must be blank |  
| `V5SB4005EH` | Customer NA account must be numeric |  
| `V5SB4008EA` | Relationship not valid for this ORG |
| `V5SB4008EB` | Relationship not valid for the dual ORG |  
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record is incomplete |
| `V5SB4009EA` | Relationship number is required | 
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |  
| `V5SB4012EA` | Sweeping not allowed in this Logo record |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |  
| `V5SB4012EC` | Account type must be zero fora prepaid account |
| `V5SB4154SA` | Customer number not on file for this ORG |
| `V5SB4154SB` | Customer number already exist for this ORG |  
| `V5SB4154SC` | Customer number must be generic for presonalized prepaid account |
| `V5SB4154SD` | Generic customer not allowed |
| `V5SB4155EA` | Customer number not on file for the dual ORG  |
| `V5SB4155EB` | Generic customer not allowed |
| `V5SB4155EC` | Customer number already exist for the dual ORG |
| `V5SB4154EA` | Invalid customer number |
| `V5SB4160EE` | Invalid customer check digit this ORG |
| `V5SB4160EG` | Invalid customer check digit dual ORG |