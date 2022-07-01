# Update Customer Demographics

This service will be used to update the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer.  The customer ID will be passed in the input request to retrieve the demographic information. 

## Endpoint

`PUT /v1/customers/{customerId}/nameAddress`

## Payload Example

### Request Payload

```json
{
  "namesData": {
    "birthName": "",
    "givenName": "ABC",
    "middleName": "",
    "nameLine1": "M S SWAMY",
    "nameLine2": "KK",
    "nameLine3": " "
  },
  "languageIndicator": "AUS",
  "homePhoneNumber": "9241800756",
  "homePhoneFlag": "0",
  "faxNumber": "82364782",
  "faxPhoneFlag": "0",
  "mobileNumber": "112233",
  "smsFlag": "0",
  "mobilePhoneFlag": "0",
  "emailAddress": "SAM@FISERV.COM",
  "birthDate": "06/04/1986",
  "isReturnMailEnabled": "Y",
  "employerData": {
    "nameOfEmployer": "Y",
    "addressLine1": "Y",
    "addressLine2": "Y",
    "phoneNumber": "Y",
    "phoneFlag": "0",
    "jobTitle": "Y"
  },
  "addressData": {
    "addressLine3": "CHITRAPURI",
    "addressLine4": "DELHI",
    "addressLine1": "FLAT NO:404",
    "addressLine2": "RAINBOW APTS",
    "city": "DELHI",
    "stateProvince": "DL",
    "countryCode": "IND",
    "postalCode": "110004",
    "houseNumber": ""
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/customers/{customerId}/nameAddress).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "addressData": {
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
  "employerData": {
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
  "namesData": {
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
  "errorCode": "V5NA0010SF",
  "errorMessage": "Update Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`V5NA4001SN` | Business unit is not numeric |
|`V5NA0010SF` | Update Request - Record not found |
|`V5NA0011SF` | Update Request - Record Add Pending |
|`V5NA4002SC` | Customer account is in purged |
|`V5NA4001SV` | Invalid business unit |  
|`V5NA0318EA` | Invalid  country  code |
|`V5NA0713EA` | Postal Code Format invalid |
|`V5NA0320EA` | Invalid  ISO language code |
|`V5NA0328SV` | Invalid Home Phone flag |
|`V5NA0334SV` | Invalid  Mobile Phone Flag |
|`V5NA0202EA` | Either of first/middle/last name is required for maker |
|`V5NA0202EB` | Either of first/middle/last name is required for maker and comaker |
|`V5NA0312SZ` | Update access not granted for Address Line 1 |
|`V5NA0313SZ` | Update access not granted for Address Line 2 |
|`V5NA0242SZ` | Update access not granted for Address Line 3 |
|`V5NA0243SZ` | Update access not granted for Address Line 4 |
|`V5NA0314SZ` | Update access not granted for City |
|`V5NA0315SZ` | Update access not granted for State/Province |
|`V5NA0202SZ` | Update access not granted for First Name |
|`V5NA0327SZ` | Update access not granted for Home Phone Number |
|`V5NA0330SZ` | Update access not granted for Fax Number |
|`V5NA0333SZ` | Update access not granted for Mobile Number |
|`V5NA0504SZ` | Update access not granted for User Defined Field 4 |
|`V5NA0419SZ` | Update access not granted for Email Address |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*