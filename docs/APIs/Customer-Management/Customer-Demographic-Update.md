# Customer Demographic Update

This service will be used to update the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer.  The customer ID will be passed in the input request to retrieve the demographic information. 

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/customers/{customerNumber}/nameAddress`

## Payload Example

### Request Payload

```json
{
  "postalCode1": "",
  "city1": "DELHI",
  "nameLine21": "KK",
  "firstName1": "ABC",
  "emailAddress1": "SAM@FISERV.COM",
  "homePhoneFlag1": "",
  "userDefinedField41": "Y",
  "middleName1": "",
  "faxNumber1": "",
  "addressLine21": "RAINBOW APTS",
  "smsFlag1": "",
  "addressLine41": "",
  "lastName1": "",
  "faxPhoneFlag1": "",
  "stateprovince1": "",
  "nameLine31": " ",
  "nameLine11": "M S SWAMY",
  "mobileNumber1": 112233,
  "countryCode1": "",
  "languageIndicator1": "",
  "addressLine31": "DELHI",
  "homePhoneNumber1": 1234567,
  "addressLine11": "FLAT NO:404",
  "houseNumber1": "",
  "mobilePhoneFlag1": "",
  "dateOfBirth1": "06/04/1986"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/customers/{customerNumber}/nameAddress).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the Card. |
| `customerNumber` | Path Variable | *string* | 19 | Customer Number of the cardholder. |

Along with above key fields any of the Name / address / Phone number / email ID information that is required to be updated.

### Successful Response Payload

```json
{
  "postalCode1": "",
  "city1": "DELHI",
  "businessUnit": 100,
  "nameLine21": "KK",
  "firstName1": "ABC",
  "emailAddress1": "SAM@FISERV.COM",
  "homePhoneFlag1": "",
  "userDefinedField41": "Y",
  "middleName1": "",
  "faxNumber1": "",
  "addressLine21": "RAINBOW APTS",
  "smsFlag1": "",
  "addressLine41": "",
  "lastName1": "",
  "faxPhoneFlag1": "",
  "stateprovince1": "",
  "nameLine31": " ",
  "nameLine11": "M S SWAMY",
  "mobileNumber1": 112233,
  "accountNumber": 1000000000150191,
  "countryCode1": "",
  "languageIndicator1": "",
  "addressLine31": "DELHI",
  "homePhoneNumber1": 1234567,
  "addressLine11": "FLAT NO:404",
  "houseNumber1": "",
  "mobilePhoneFlag1": "",
  "dateOfBirth1": "06/04/1986"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5NA4001SN",
  "errorMessage": "Business unit is not numeric"  
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