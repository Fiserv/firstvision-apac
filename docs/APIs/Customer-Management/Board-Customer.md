# Board Customer

This API is used to board the new customer in real time. 

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/customers/boardCustomer`

## Payload Example

### Request Payload

```json
{
  "dualFlag": 0,
  "postalCode1": 112345,
  "city1": "La Vegas",
  "nameLine21": " Jacob ",
  "businessUnit": 600,
  "firstName1": " Samuel",
  "state1": "California",
  "middleName1": " ",
  "email1": "abc@goole.com",
  "addressLine21": " S.H. Qo",
  "addressLine41": "USA",
  "lastName1": "Christopher",
  "nameTypeInd21": 0,
  "employeePhone1": 67894,
  "nameLine31": "Samuel",
  "nameLine11": "John",
  "product": 600,
  "gender1": 1,
  "title1": "ADWSQQ",
  "mobileNumber1": 11231232,
  "homePhone1": 11230342,
  "nationalId1": "2363-12-2839-1",
  "countryCode1": "USA ",
  "residenceFlag1": 1,
  "altEmail1": "abc1@google.com",
  "addressLine31": "California",
  "addressLine11": "House No. 12",
  "emailFlag1": 1,
  "nameTypeInd31": 0,
  "nameTypeInd11": 0,
  "dateOfBirth1": "01/02/2010"
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/customers/boardCustomer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `Business Unit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `Product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |
| `Dual Flag` | Payload | *number* | 1 | This field indicates whether CMS adds a duplicate customer  record in the associated business unit for dual currency processing. |
| `Title` | Payload | *string* | 20 | Customer title. |
| `Name Type Ind***` | Payload | *number* | 1 | Name Type indiacators 1/2/3. |
| `Name Line***` | Payload | *string* | 40 | Customer name line 1/2/3. |
| `Address Line***` | Payload | *string* | 40 | Customer address line 1/2/3/4. |
| `City` | Payload | *string* | 30 | Name of customer city. |
| `State` | Payload | *string* | 30 | Name of state. |
| `Postal Code` | Payload | *string* | 10 | Postal code. |
| `Country Code` | Payload | *string* | 03 | code of country. |
| `Residence Flag` | Payload | *number* | 1 | Residential status. |
| `Home Phone` | Payload | *string* | 20 | Residential phone number. |
| `Employee Phone` | Payload | *string* | 20 | Employee phone number. |
| `Date of Birth` | Payload | *date* | DD/MM/YYYY | Customer date of birth. |
| `Last Name` | Payload | *string* | 40 | Last name of customer. |
| `Middle Name` | Payload | *string* | 40 | Middle name of customer. |
| `First Name` | Payload | *string* | 40 | First name of customer. |
| `National ID` | Payload | *string* | 25 | Customer national ID number. |
| `Gender` | Payload | *number* | 1 | Gender of customer. |
| `E-Mail` | Payload | *string* | 60 | customer primary mail id. |
| `Alt E-Mail` | Payload | *string* | 50 | Customer alternate mail id. |
| `Mobile Number` | Payload | *string* | 20 | Customer mobile number. |
| `E-Mail Flag` | Payload | *number* | 1 | This is the code that indicates to select mail id for communication.|

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "customerNumber": 0000000001000000007
}
```

### Error Response Payload

```json
{
   "errorCode" :  "V5SB4003EA" ,
   "errorMessage" : "Base account number is required"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4003EA` | Base account number is required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number is required |
| `V5SB4005EA` | Customer NA account must be blank | 
| `V5SB4005EB` | Customer NA account required |
| `V5SB4005EG` | Customer NA account must be blank |  
| `V5SB4005EH` | Customer NA account must be numeric |  
| `V5SB4008EA` | Relationship not valid for this ORG |
| `V5SB4008EB` | Relationship not valid for the dual ORG |  
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record is incomplete |
| `V5SB4009EA` | Relationship number is required | 
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |  
| `V5SB4012EA` | Sweeping not allowed in this Logo record |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |  
| `V5SB4012EC` | Account type must be zero fora prepaid account |
| `V5SB4154SA` | Customer number not on file for this ORG |
| `V5SB4154SB` | Customer number already exist for this ORG |  
| `V5SB4154SC` | Customer number must be generic for presonalized prepaid account |
| `V5SB4154SD` | Generic customer not allowed |
| `V5SB4155EA` | Customer number not on file for the dual ORG  |
| `V5SB4155EB` | Generic customer not allowed |
| `V5SB4155EC` | Customer number already exist for the dual ORG |
| `V5SB4154EA` | Invalid customer number |
| `V5SB4160EE` | Invalid customer check digit this ORG |
| `V5SB4160EG` | Invalid customer check digit dual ORG |