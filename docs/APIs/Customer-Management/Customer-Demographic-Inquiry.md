# Inquire Customer

This service will be used to enquire the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer.  The customer ID will be passed in the input request to retrieve the demographic information. 

## Endpoint

`GET /v1/customers/{customerId}/nameAddress`

## Payload Example

### Request Payload

>Should be empty.  
>
>***Customer Identification should be sent as Path Variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/nameAddress).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Successful Response Payload

```json
{
  "addressDetails": {
    "addressLine1": "FLAT NO:404",
    "addressLine2": "RAINBOW APTS",
    "addressLine3": "CHITRAPURI",
    "addressLine4": "DELHI",
    "city": "DELHI",
    "countryCode": "IND",
    "houseNumber": " ",
    "postalCode": "110004",
    "stateProvince": "DL"
  },
  "birthDate": "06/04/1986",
  "businessUnit": 200,
  "customerId": "0000020000065439605",
  "emailAddress": "SAM@FISERV.COM",
  "employerDetails": {
    "addressLine1": "Y",
    "addressLine2": "Y",
    "jobTitle": "Y",
    "nameOfEmployer": "Y",
    "phoneFlag": "0",
    "phoneNumber": "Y"
  },
  "faxNumber": "82364782",
  "faxPhoneFlag": "0",
  "homePhoneFlag": "0",
  "homePhoneNumber": "9241800756",
  "isReturnMailEnabled": "Y",
  "languageIndicator": "AUS",
  "mobileNumber": "112233",
  "mobilePhoneFlag": "0",
  "namesDetails": {
    "birthName": " ",
    "givenName": "ABC",
    "middleName": " ",
    "nameLine1": "M S SWAMY",
    "nameLine2": "KK",
    "nameLine3": " "
  },
  "smsFlag": "0"
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
|`V5NA4002SA` | Customer account not found|
|`V5NA4002SB` | Customer account is in add pending|
|`V5NA4002SC` | Customer account is purged|
|`V5NA0004SF` | Get  request - Record not found|
|`V5NA0005SF` | Get request - Record add pending|

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*