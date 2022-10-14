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
  "dualFlag": "0",
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
  "addressData": {
    "addressLine1": "House No. 12",
    "addressLine2": "S.H. Qo",
    "addressLine3": "California",
    "addressLine4": "USA",
    "city": "La Vegas",
    "state": "CL",
    "postalCode": "112345",
    "countryCode": "USA"
  },
  "namesData": {
    "nameLine1": "John",
    "nameLine2": "Jacob ",
    "nameLine3": "Samuel",
    "birthName": "Christopher",
    "middleName": " ",
    "givenName": "Samuel"
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
  "customerId": "0006000012000000846"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/customers/boardCustomer",
    "invalid-params": [
        "V5S84152EB: ORG DOES NOT ALLOW ACCOUNT NUMBER GENERATION"
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
| `V5S84005EA` | Customer NA account must be blank |                                
| `V5S84003EA/V5S84003EE` | Base account number required |                                     
| `V5S84150EE` | Customer NA account and base account are equal |                   
| `V5S84005EB` | Customer NA account required |                                     
| `V5S84005EG` | Customer NA account must be blank |                                
| `V5S84003EG` | Base account number must be numeric |                              
| `V5S84150EG` | Customer NA account and base account are equal |                  
| `V5S84005EH` | Customer NA account must be numeric |                              
| `V5S84003EH` | Base account number required | 
| `V5S84154SA` | Customer number not on file for this org |                         
| `V5S84154SB` | Customer number already exists for this org | 
| `V5S84157EA` | Base account number already exists for this org |                  
| `V5S84157EC` | Account nbr exist on relationship file for this org |              
| `V5S84158EA` | Account nbr cannot duplicate existing embosser for this org |      
| `V5S84151EE` | Maximum number of 20 attempts made on base account number |        
| `V5S84152EC` | Maximum number of 20 attempts made on customer number |            
| `V5S84152EE` | Generated relationship number is less than beginning range |       
| `V5S84162SB` | DDA/savings routing information is required |                      
| `V5S89909SA` | CCID should not be spaces or zeroes |                              
| `V5S89910SA` | Address id should not be spaces or zeroes |                        
| `V5S89516SB` | ACCT CCID should contain only alphanumeric |                
| `V5S89517SB` | ACCT addrid should contain only alphanumeric chars and '-' |
| `V5S89519SA` | Card CCID should contain only alphanumeric |                
| `V5S89518SB` | Card addrid should contain only alphanumeric chars and '-' |
| `V5S84004SK` | CGID/customer number should be numeric |        
| `V5NA0419ED` | Email cont ind not active |                                        
| `V5NA0333EE/V5NA0419EE` | SMS ind not active |
| `V5NA0419EF` | Email cont ind not active |                                        
| `V5NA4002EB` | Nbr already exists on relationship file |                          
| `V5NA0332EA` | Mobile number is required when SMS ind flag is 1 |                 
| `V5NA0333EA/V5NA0333EB/V5NA0333EC` | Mobile number not found |
| `V5NA0333ED` | Mobile number required |                                           
| `V5NA0419EA/V5NA0419EB/V5NA0419EC` | Email address not found |       
| `V5NA4001SI` | Org does not allow cust nbr generation |                           
| `V5NA4001SJ` | Max nbr of 20 attempts made on cust nbr |                          
| `V5NA4001SK` | Customer number generation error |                                 
| `V5NA4001SL` | Generated cust nbr is greater than ending cust nbr |               
| `V5NA4002SA` | AMNA - account not found |                                         
| `V5NA4002SB` | AMNA - account is in add pending |                                 
| `V5NA0519EB` | End date must be greater than start date |                         
| `V5NA9901EX` | Field not maintaiNAble when name type ind > 0 |                    
| `V5NA0202EA` | Either of first/middle/last name is required for maker |           
| `V5NA0327EA` | Home phone is required when call ind flag is 1 |                  
| `V5NA0330EA` | Fax phone is required when fax ind flag is 1 |                    
| `V5NA0333EH` | Mobile number is required when call ind flag is 1 |               
| `V5NA0414EA` | Employer phone required when work phone flag is 1 |               
| `V5NA0419EG` | Email id is required when mail ind flag is 1 |                    
| `V5NA4081EA` | First name is required |                                          
| `V5A34058SB` | Customer number not found |                                       
| `V5DB4001SD` | Customer number can not be spaces |                                
| `V5DB4001AS` | Cust nbr not found |                                               
| `V5DB4001SC` | AMBX rec not found |                                               
| `V5DB4001SE` | AMBS rec not found |                                               
| `V5DB4001SF` | Account not found amax |                                           
| `V5DB4001SH` | AMED record not found |                                            
| `V5DB4001SJ` | ZAMDX rec not found |                                              


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*