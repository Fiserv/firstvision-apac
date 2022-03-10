# Search Customers

This service is used to retrieve customer's information based on primary and optional search values like Last name, Indentification number, Phone number etc.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/customers/searchCustomer`

## Payload Example

### Request Payload

```json
{
  "lastName": "",
  "primaryDataSwitch": 1,
  "businessUnit": 0,
  "user15": "",
  "user14": "",
  "postalCode": "",
  "dateOfBirth": "1970-01-01",
  "title": "",
  "suffix": "",
  "primaryData": 390539172,
  "firstName": "",
  "phoneNumber": "",
  "mobileDeviceId": "",
  "countryCode": "",
  "identificationNumber": "",
  "middleName": "",
  "optionalDataMatch": 1
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/searchCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `Primary Data Switch` | Payload | *string* | 01 | A primary search value must be supplied, and can be based on one of four fields - last/business/generic/store name, identification number, phone number, postal code or mobile device id. |
| `Primary Data` | Payload | *string* | 40 | Search field as per Primary data switch. |
| `Optional Data Match` | Payload | *string* | 1 | This is the code that indicates whether to add a new account record. |
| `First Name` | Payload | *string* | 40 | First name of the customer. |
| `Middle Name` | Payload | *string* | 40 | Middle name of the customer. |
| `Last Name` | Payload | *string* | 40 | Last name of the Customer. |
| `Identification Number` | Payload | *string* | 25 | Code that indicates if this number is a Social Security number or other tax identification number. |
| `Phone Number` | Payload | *string* | 20 | Phone Number of Customer. |
| `Postal Code` | Payload | *string* | 10 | Postal code portion of the mailing address of the owner. |
| `Mobile Device ID` | Payload | *string* | 20 | Identification of a mobile device associated with a mobile payment instrument (PI) embosser. CMS does not validate this field; it is stored only. |
| `Date Of Birth` | Payload | *date* | DD/MM/YYYY | Date of Birth of Customer. Format is DD/MM/YYYY. |
| `Title` | Payload | *string* | 20 | Professional or honorary title of the customer. |
| `Suffix` | Payload | *string* | 20 | Suffix for the customer. Examples include Jr., Sr., etc. |
| `Country Code` | Payload | *string* | 3 | Country for the customer. If you use this field, enter the exact country code. |
| `User 14` | Payload | *string* | 20 | User-defined field for the search. This field literal displays as User 14 unless changed on the Organization record. |
| `User 15` | Payload | *string* | 20 | User-defined field for the search. This field literal displays as USER 15 unless changed on the Organization record. |
| `Business Unit` | Payload | *number* | 03 | Identification number associated with this Account Base Segment record, the values are 001–998. |
| `Key Value` | Payload | *string* | 40 | Key Value. |
| `Key Tie Breaker` | Payload | *number* | 08 | Key Tie Breaker. |
| `When Other` | Payload | *string* | 01 | When Other. |
| `Customer Name Extended Lookup` | Payload | *string* | 442 | Customer Name Extended Lookup. |

### Successful Response Payload

```json
{
  "country": "",
  "lastName": "",
  "businessUnit": 0,
  "user15": "",
  "user14": "",
  "postalCode": "",
  "dateOfBirth": "01/09/1990",
  "title": "",
  "suffix": "",
  "token": [
    {
      "country": "",
      "businessUnit": 600,
      "user15": "",
      "user14": "",
      "postalCode": "",
      "nameField": "MR CRUOSAREOBUCDK C CUACOEBKNQ",
      "lastbusinesstoregenricName": "CUACOEBKNQJRXD",
      "dateOfBirth": "24/04/1990",
      "suffix": "",
      "title": "",
      "nameAndOtherDetails": "CUACOEBKNQJRXD/CRUOSAREOBUCDK/C/390539172/          /0000000 ///////",
      "firstName": "CRUOSAREOBUCDK",
      "sourceCode": "O2",
      "phoneNumber": 950340942,
      "custstoremerch": 1000000024,
      "identificationNumber": 390539172,
      "middleName": "C"
    }
  ],
  "firstName": "",
  "phoneNumber": "",
  "mobileDeviceId": "",
  "primaryKeyField": 390539172,
  "countryCode": "",
  "identificationNumber": "",
  "middleName": ""
}
```

### Error Response Payload

```json
{
   errorCode" :  V5XL4001SA" ,
   errorMessage" : Customer search screen is not available"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5XL4001SA` | Customer search screen is not available |
| `V5XL4001SB` | Primary search option  for MOB DEV ID is inactive on system record |
| `V5XL4001SF` | Primary search option  field must equal to 0,1,2,3,4 |
| `V5XL4001SC` | Primary search option  for postal code is inactive on system record |
| `V5XL4001SD` | Primary search option  for phone number inactive on system record |
| `V5XL4001SE` | Primary search option  for ID number inactive on system record |                               
| `V5XL4002EA` | First Character cannot be  a space |          
| `V5XL4002EB` | First Character cannot be  asterick |
| `V5XL4002EP` | No result found for this search criteria | 
| `V5XL4002SL` | MOB DEV ID primary option search invalid |                    
| `V5XL4002SK` | Postal code primary option search invalid |                        
| `V5XL4002SJ` | phone number primary option search invalid |                       
| `V5XL4002SI` | Identification number primary option search invalid |              
| `V5XL4002SH` | Last Name primary option search invalid |              
| `V5XL4002SG` | Cannot have asterix only as search criteria |                       
| `V5XL4002SM` | Primary data Switch is on, valid primary data should be entered |       
| `V5XL4002SE` | Minimum number of character required for LBSG name |      
| `V5XL4002SD` | Minimum number of character required for ID number |
| `V5XL4002SC` | Minimum number of character required for phone number |            
| `V5XL4002SB` | Minimum number of character required for postal code |           
| `V5XL4002SN` | Minimum number of character required for MOBILE DEVICE ID |       
| `V5XL4002EO` | Invalid primary search data |
| `V5XL4003SA` | Service function code invalid |                                    
| `V5XL4003SF` | Invalid SVC function code |
| `V5XL4003SB` | Valid value for optional data match is 0 or 1 |