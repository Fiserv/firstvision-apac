# Board Card

Board Card API allows to create a new card for an existing account. This API can be invoked with required fields and new card can be generated in real time mode.

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/cards/boardCard`

## Payload Example

### Request Payload

```json
{
  "businessUnit": 600,
  "mccGroupLimits": " ",
  "cardholderFlag": 0,
  "city": " ",
  "typeCardMailer": 0,
  "postalCode": 1231,
  "savingsAccountNbr": " ",
  "visaMiniIndicator": " ",
  "mobileDeviceId": 12343,
  "posServiceCode": 0,
  "addressLine1": "House no. 12 ",
  "addressLine2": "St. Paul Road ",
  "mobileProvisionStatus": 0,
  "embossedName2": "Samuel Baro",
  "requestedCardType": 0,
  "product": 600,
  "embossedName1": "John Brono ",
  "tempCardNbr": " ",
  "name1TypeIndicator": 0,
  "cardSequence": 1,
  "typeOfCard": 0,
  "plasticId": " ",
  "name2TypeIndicator": 0,
  "customerNumber": 9006000000000300000,
  "stateprovince": "Utah",
  "chequeAccountNbr": " ",
  "suppressLetter": " ",
  "baseAccountNumber": 4440010000000017,
  "cardAction": 0,
  "numberOfCardsRequested": 0,
  "createEmbosserRecords": "Y",
  "name2": "QWER",
  "deviceIndicator": " ",
  "name1": "ABCD",
  "programId": 0
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/boardCard).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `baseAccountNumber` | Payload | *string* | 19 | This is an identification number to assign to the new account base segment record.|
| `createEmbosserRecords` | Payload | *string* | 01 | This is the code that indicates whether to add a new embosser record. |
| `customerNumber` | Payload | *string* | 19 | Number that identifies the Customer Name/Address record of the account holder. |
| `businessUnit` | Payload | *number* | 03 | Identification number associated with this account base segment record, the values are 001–998. |
| `product` | Payload | *number* | 03 | Identification number of the product associated with the  account or relationship. | |

### Successful Response Payload

```json
{
  "expiryDate": "01/10/2025",
  "product": 1,
  "businessUnit": 600,
  "cardActivationStatus": " ",
  "tempCardNbr": " ",
  "nameOnCard": "JOHN",
  "maskedPanNumber": 4440010847192688,
  "cardNumberfvToken": 4440010847192688
}
```

### Error Response Payload

```json
{
   errorCode" :  V5SB4003EA" ,
   errorMessage" : Base Account Number is requsted"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4003EA` | Base account number is requsted |
| `V5SB4003EG` | Base account number must be numeric | 
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer NA account must be blank | 
| `V5SB4005EB` | Customer NA account required |
| `V5SB4005EG` | Customer NA account must be blank | 
| `V5SB4005EH` | Customer NA account must be numeric | 
| `V5SB4008EA` | Relationship not Valid for this ORG |
| `V5SB4008EB` | Relationship not Valid for the DUAL ORG | 
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | LOGO Record not on File |
| `V5SB4002EB` | LOGO Record is incomplete | 
| `V5SB4009EA` | Relationship number required | 
| `V5SB4011EA` | Insurance not allowed for prepaid accounts | 
| `V5SB4012EA` | Sweeping not allowed this LOGO |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 | 
| `V5SB4150EI` | No embosser record allowed for control account |
| `V5SB4150EJ` | No embosser record allowed for diversion account | 
| `V5SB4150EK` | No embosser record allowed for billing account |
| `V5AP4061EA` | Number cards required must equal 0 OR 1 |
| `V5AP4063EA` | Embossed name type must not equal 3 |
| `V5AP4088EA` | Card delay days value must be numeric | 
| `V5AP4097SA` | Card number and account number must be equal for card scheme | 
| `V5AP4101SA` | Card number check digit is invalid |
| `V5AP4105SA` | Card sequence already atmaximum for card number | 
| `V5AP4106SA` | Card sequence already atmaximum for chip card number |