# Board Card

Board Card API allows to create a new card for an existing account. This API can be invoked with required fields and new card can be generated in real time mode.

Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`POST /v1/cards/boardCard`

## Payload Example

### Request Payload

```json
{
  "accountId": "0006000012000000263",
  "businessUnit": 600,
  "productId": 1,
  "customerId": "0006000012000000256",
  "cardAction": "0",
  "numberOfCardsRequested": 0,
  "cardType": 0,
  "requestedCardType": 0,
  "cardMailerType": 0,
  "plasticId": " ",
  "name1TypeIndicator": "0",
  "name2TypeIndicator": "0",
  "posServiceCode": 0,
  "cardholderFlag": "0",
  "visaMiniCardVersion": "0",
  "programId": 0,
  "mobileDeviceId": "12343",
  "mobileProvisionStatus": "0",
  "deviceIndicator": "0",
  "mccGroupLimits": " ",
  "chequeAccountId": " ",
  "savingsAccountId": " ",
  "namesData": {
    "embossedName1": "John Brono ",
    "embossedName2": "Samuel Baro",
    "name1": "ABCD",
    "name2": "QWER"
  },
  "addressData": {
    "addressLine1": "House no. 12 ",
    "addressLine2": "St. Paul Road ",
    "city": " ",
    "stateprovince": "Uth",
    "postalCode": "1231",
    "addressId": "13"    
  }
  "physicalVirtualIndicator": "P",
  "isDynamicCVV2Enabled": "0
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/boardCard).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 03 | Unique identification number associated with the organization. Valid values from 001-998. |
| `productId` | Payload | *number* | 03 | Unique identification number of the product associated with the organization. Valid values are 001-998. | 
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `customerId` | Payload | *string* | 19 | Unique identification number assigned to a customer. |
| `embossedName1` | Payload | *string* | 26 | Name to be embossed on the first embossing line of the card. |

### Successful Response Payload

```json
{
  "activationStatus": "0",
  "businessUnit": 600,
  "expiryDate": "18/01/2024",
  "externalCustomerId": "99000001234501",
  "maskedPaymentCardNumber": "0004440010737034347",
  "nameOnCard": "John Brono",
  "paymentInstrumentId": "0004440010737034347",
  "productId": 1
}
```

### Error Response Payload

```json
[
  {
    "errorCode": "440401",
    "detail": "Please refer to invalid-params for error details",
    "title": "Not found",
    "instance": "/v1/cards/boardCard",
    "source": "VPL",
    "status": 404,
    "invalid-params": [
        "V5AK4056SA: ORG/ACCOUNT NUMBER COMBINATION NOT FOUND"
    ]
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5AK4056SA` | Org/Account number combination not found |
| `V5SB4003EA` | Base account number is requsted |
| `V5SB4003EG` | Base account number must be numeric | 
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer na account must be blank | 
| `V5SB4005EB` | Customer na account required |
| `V5SB4005EG` | Customer na account must be blank | 
| `V5SB4005EH` | Customer na account must be numeric | 
| `V5SB4008EA` | Relationship not valid for this org |
| `V5SB4008EB` | Relationship not valid for the dual org | 
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `s4002EB` | Logo record is incomplete | 
| `V5SB4009EA` | Relationship number required | 
| `V5SB4011EA` | Insurance not allowed for prepaid accounts | 
| `V5SB4012EA` | Sweeping not allowed this logo |
| `V5SB4012EB` | Hcs must be active for account type values 1,2,3 | 
| `V5SB4150EI` | No embosser record allowed for control account |
| `V5SB4150EJ` | No embosser record allowed for diversion account | 
| `V5SB4150EK` | No embosser record allowed for billing account |
| `V5AP4061EA` | Number cards required must equal 0 or 1 |
| `V5AP4063EA` | Embossed name type must not equal 3 |
| `V5AP4088EA` | Card delay days value must be numeric | 
| `V5AP4097SA` | Card number and account number must be equal for card scheme | 
| `V5AP4101SA` | Card number check digit is invalid |
| `V5AP4105SA` | Card sequence already atmaximum for card number | 
| `V5AP4106SA` | Card sequence already atmaximum for chip card number |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*