# Customer Demographic Inquiry

This service will be used to enquire the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer.  The customer ID will be passed in the input request to retrieve the demographic information. 

## Endpoint

`GET /v1/customers/{customerNumber}/nameAddress`

## Payload Example

### Request Payload

>Should be empty.  
***Customer Number should be sent as Path Variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/nameAddress).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | Customer number of the cardholder. |

### Successful Response Payload

```json
{
  "addressLine1": "FLAT NO:404",
  "addressLine2": "RAINBOW APTS",
  "addressLine3": "DELHI",
  "addressLine4": "",
  "businessUnit": 200,
  "city": "DELHI",
  "countryCode": "",
  "customerNumber": "0000020000066806355",
  "dateOfBirth": "06/04/1986",
  "emailAddress": "SAM@FISERV.COM",
  "faxNumber": "",
  "faxPhoneFlag": "0",
  "firstName": "ABC",
  "homePhoneFlag": "0",
  "homePhoneNumber": "1234567",
  "houseNumber": "",
  "languageIndicator": "AUS",
  "lastName": "",
  "middleName": "",
  "mobileNumber": "112233",
  "mobilePhoneFlag": "0",
  "nameLine1": "M S SWAMY",
  "nameLine2": "KK",
  "nameLine3": "",
  "postalCode": "",
  "smsFlag": "0",
  "stateProvince": "",
  "userDefinedField4": "Y"
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
|`V5NA0005SF` | Get Request - Record add pending|