# Board Customer

This API is used to create a new customer Id with customer's demographic details. 

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/customers/boardCustomer`

## Payload Example
 
<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "customerId": "0000000993456711108",
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

<!--
type: tab
--> 

```json
{
  "businessUnit": 600,
  "customerId": "0006000012000000846"
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

<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/boardCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Payload | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |
| `firstName` | Payload | *string* | 40 | First name of customer. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S84152EB` | Org does not allow account number generation |
| `V5S84001SA` | Organization not on file |
| `V5S84002EA` | Logo record not on file |
| `V5S84002EB` | Logo record incomplete | 
| `V5S84154SA` | Customer number not on file for this org |
| `V5S84154SB` | Customer number already exists for this org | 
| `V5S84154SD` | Generic Customer not allowed |
| `V5S84155EA` | Customer number not on file for the dual org | 
| `V5S84155EB` | Generic Customer not allowed |
| `V5S84155EC` | Customer number already exists for the dual org |
| `V5S84154EA` | Invalid Customer number | 
| `V5S84160EE` | Invalid Customer check digit for this org |                         
| `V5S84160EG` | Invalid Customer check digit for dual org |
| `V5NA4081EA` | First name is required |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*