# Search Customers

This service is used to retrieve customer's information based on primary and optional search values like Last name, Indentification number, Phone number etc.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/customers/searchCustomer`

## Payload Example

### Request Payload

```json
{
  "customerSearchReq": {
    "primaryDataSwitch": "0",
    "primaryData": "Test*",
    "optionalDataMatch": "1"
  },
  "optionalDataReq": {
    "firstNameOfCust": "",
    "middleNameOfCust": "",
    "lastNameOfCust": "",
    "identificationNumberOfCust": "",
    "phoneNumberOfCust": "",
    "postalcodeOfCust": "",
    "mobileDeviceIDOfCust": "",
    "dateOfBirthOfCust": "0",
    "titleOfCust": "",
    "suffixNameOfCust": "",
    "countryCodeOfCust": "",
    "user14OfCust": "",
    "user15OfCust": "",
    "businessUnitOfCust": 0
  }
}

``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/searchCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `primaryDataSwitch` | Payload | *string* | 01 | A primary search value must be supplied, and can be based on one of four fields - last/business/generic/store name, identification number, phone number, postal code or mobile device id. |
| `primaryData` | Payload | *string* | 40 | Search field as per Primary data switch. |
| `optionalDataMatch` | Payload | *string* | 1 | This is the code that indicates whether to add a new account record. |

### Successful Response Payload

```json
{
  "customerlistRes": [
    {
      "businessUnit": 200,
      "country": " ",
      "cust/Store/Merchant": "0002000000050623496",
      "dateOfBirth": "09011985",
      "firstName": "CMS Fiserv",
      "identificationNumber": "0050623496",
      "last/Business/Store/GenericName": "Test 01",
      "middleName": " ",
      "nameAndOtherDetails": "Test/CMS//0050623496/             /9011985 ////6430///",
      "nameField": "Ms CMS Test 01",
      "phoneNumber": "0000000000000",
      "postalCode": "6430",
      "sourceCode": "O1",
      "suffix": " ",
      "title": " ",
      "user14": " ",
      "user15": " "
    },
    {
      "businessUnit": 200,
      "country": " ",
      "cust/Store/Merchant": "0002000000050623502",
      "dateOfBirth": "00000000",
      "firstName": "CMS Fiserv",
      "identificationNumber": "0050623502",
      "last/Business/Store/GenericName": "Test 02",
      "middleName": " ",
      "nameAndOtherDetails": "Test/CMS//0050623502/             /0000000 ////4000///",
      "nameField": "Mr CMS Fiserv Test 02",
      "phoneNumber": "0061411075763",
      "postalCode": "4000",
      "sourceCode": "O1",
      "suffix": " ",
      "title": " ",
      "user14": " ",
      "user15": " "
    },
    {
      "businessUnit": 200,
      "country": " ",
      "cust/Store/Merchant": "0002000000050625775",
      "dateOfBirth": "19081967",
      "firstName": "CMS",
      "identificationNumber": "0050625775",
      "last/Business/Store/GenericName": "Testing",
      "middleName": " ",
      "nameAndOtherDetails": "Testing/CMS//0050625775/            /9081967 ////0801///",
      "nameField": "CMS Testing",
      "phoneNumber": "+61427507154",
      "postalCode": "0801",
      "sourceCode": "O1",
      "suffix": " ",
      "title": " ",
      "user14": " ",
      "user15": " "
    }
  ]
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