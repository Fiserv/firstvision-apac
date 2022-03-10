# Customer Demographic Inquiry

This service will be used to enquire the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer.  The customer ID will be passed in the input request to retrieve the demographic information. 

## Endpoint

`GET /v1/customers/{customerNumber}/nameAddress`

## Payload Example

### Request Payload

>Shoud be empty.  
***Customer Number should be sent as Path Variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/nameAddress).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the card. |
| `customerNumber` | Path Variable | *string* | 19 | Customer number of the cardholder. |

### Successful Response Payload

```json
{
  "accountNumber": "0001000000000150191",
  "addressLine11": "",
  "addressLine21": "",
  "addressLine31": "",
  "addressLine41": "",
  "businessUnit": "100",
  "city1": "",
  "countryCode1": "",
  "dateOfBirth1": "00/00/0000",
  "emailAddress1": "SAM@FISERV.COM",
  "faxNumber1": "",
  "faxPhoneFlag1": "0",
  "firstName1": "ABC",
  "homePhoneFlag1": "0",
  "homePhoneNumber1": "1234567",
  "houseNumber1": "",
  "languageIndicator1": "",
  "lastName1": "",
  "middleName1": "",
  "mobileNumber1": "112233",
  "mobilePhoneFlag1": "0",
  "nameLine11": "",
  "nameLine21": "",
  "nameLine31": "",
  "postalCode1": "",
  "sMSFlag1": "0",
  "stateProvince1": "",
  "userDefinedField41": "Y"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5NA4002SA",
  "errorMessage": "Customer account not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`V5NA4001SV` | Invalid business unit|  
|`V5NA4002SA` | Customer account not found|
|`V5NA4002SB` | Customer account is in add pending|
|`V5NA4002SC` | Customer account is purged|
|`V5NA0004SF` | Get  Request - Record not found|
|`V5NA0005SF` | Get Request - Record Add Pending|