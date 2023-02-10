# Inquire Customer

This API used to fetch the customer demographic details such as Name / Address / Phone Number / Email ID/ Date of Birth of the given customer Id. 

## Endpoint

`GET /v1/customers/{customerId}/nameAddress`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***Customer Identification should be sent as Path Variable.***

<!--
type: tab
--> 

```json
{
  "addressDetails": {
    "addressLine1": "FLAT NO:404",
    "addressLine2": "RAINBOW APTS",
    "addressLine3": "CHITRAPURI",
    "addressLine4": "DELHI",
    "city": "DELHI",
    "countryCode": "IND",
    "county": "EMEA",
    "houseNumber": "",
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
    "phoneExtension": "801",
    "phoneFlag": "0",
    "phoneNumber": "Y"
  },
  "externalId": "1234",
  "faxNumber": "82364782",
  "faxPhoneFlag": "0",
  "homePhoneFlag": "0",
  "homePhoneNumber": "9241800756",
  "isReturnMailEnabled": "Y",
  "languageIndicator": "AUS",
  "mobileNumber": "112233",
  "mobilePhoneFlag": "0",
  "namesDetails": {
    "birthName": "",
    "givenName": "ABC",
    "middleName": "",
    "nameLine1": "M S SWAMY",
    "nameLine2": "KK",
    "nameLine3": ""
  },
  "smsFlag": "0",
  "typeOfExternalId": "1",
  "vacationDetails": {
    "countryCode": "AUS",
    "endDate": "01/01/2023",
    "phoneNumber": "8946274878",
    "startDate": "01/01/2019"
  }
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
    "instance": "/v1/customers/0000020000065439601/nameAddress",
    "invalid-params": [
      "V5NA0010SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/nameAddress).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`V5NA0010SF` | Get Request - Record not found|
|`V5NA4002SA` | Customer account not found|
|`V5NA4002SB` | Customer account is in add pending|
|`V5NA4002SC` | Customer account is purged|
|`V5NA0004SF` | Get  request - Record not found|
|`V5NA0005SF` | Get request - Record add pending|

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*