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
  "cardAction": "1",
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
  "nameDetails": {
    "embossedName1": "John Brono ",
    "embossedName2": "Samuel Baro",
    "name1": "ABCD",
    "name2": "QWER"
  },
  "addressDetails": {
    "addressLine1": "House no. 12 ",
    "addressLine2": "St. Paul Road ",
    "city": " ",
    "stateprovince": "Uth",
    "postalCode": "1231",
    "addressId": " "
  },
  "physicalVirtualIndicator": "P",
  "isDynamicCVV2Enabled": "0",
  "externalContractId": "000012672379"
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
  "businessUnit": 600,
  "productId": 1,
  "paymentInstrumentId": "0004440010057325150",
  "maskedPaymentCardNumber": "",
  "nameOnCard": "JOHN",
  "expiryDate": "01/10/2025",
  "activationStatus": "0"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/boardCard",
    "invalid-params": [
      "V5S84001EA: ORGANIZATION NOT ON FILE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5S84005EA` | Customer NA account must be blank |                                
| `V5S84003EA/V5S84003EE` | Base account number required |                                     
| `V5S84150EE` | Customer NA account and base account are equal |                   
| `V5S84005EB` | Customer NA account required |                                     
| `V5S84005EG` | Customer NA account must be blank |                                
| `V5S84003EG` | Base account number must be numeric |                              
| `V5S84150EG` | Customer NA account and base account are equal |                  
| `V5S84005EH` | Customer NA account must be numeric |                              
| `V5S84003EH` | Base account number required |      
| `V5S84154SA` | Customer number not on file for this org |                         
| `V5S84154SB` | Customer number already exists for this org |    
| `V5S84157EA` | Base account number already exists for this org |                  
| `V5S84157EC` | Account nbr exist on relationship file for this org |              
| `V5S84158EA` | Account nbr cannot duplicate existing embosser for this org |      
| `V5S84151EE` | Maximum number of 20 attempts made on base account number |        
| `V5S84152EC` | Maximum number of 20 attempts made on customer number |            
| `V5S84152EE` | Generated relationship number is less than beginning range |       
| `V5S84162SB` | DDA/savings routing information is required |                      
| `V5S89909SA` | CCID should not be spaces or zeroes |                              
| `V5S89910SA` | Address id should not be spaces or zeroes |                        
| `V5S89516SB` | ACCT CCID should contain only alphanumeric |                
| `V5S89517SB` | ACCT addrid should contain only alphanumeric chars and '-' |
| `V5S89519SA` | Card CCID should contain only alphanumeric |                
| `V5S89518SB` | Card addrid should contain only alphanumeric chars and '-' |
| `V5S84004SK` | CGID/customer number should be numeric |        
| `V5ED0204EC` | Card cannot be reissued |                                          
| `V5ED0204ED` | Card action must be less than 7 |                                  
| `V5ED0204EE` | Additional card not allowed for smart card |                       
| `V5ED0204EF` | Cannot reissue embosser with status of s |                         
| `V5ED0204EH` | This field must be 0 for a foreign account |                       
| `V5ED0204EJ` | Action of 1 allowed only if nbr outst and dte last plastic are 0 | 
| `V5ED0204EN` | Nbr of outstanding cards can not be maintaible for card action |   
| `V5ED0204EO` | Add is not allowed on nbr of outstanding cards flag |              
| `V5ED0205EA` | This field must be 0 for a foreign account |                       
| `V5ED0211EA` | Add line 1 cannot = spaces if city, state, pstl cde not = spaces | 
| `V5ED0221EB` | Cardholder flag must be zero for card scheme 0 |                   
| `V5ED0222EA` | Embosser name 1 reqd and cannot equal spaces |                     
| `V5ED0222EB` | Value is required and cannot equal spaces |                        
| `V5ED0223EA` | Value is required and cannot equal spaces                        
| `V5ED0230EA` | Mini card processing inactive for logo |                           
| `V5ED0232EB/V5ED0233EE/V5ED233EE` | Personalized cards not allowed |                                   
| `V5ED0232ED/V5ED232ED/V5ED0233ED/V5ED233ED` | Non personalized cards not allowed |   
| `V5ED0234EB/V5ED234EA` | Form factors processing inactive for logo |                        
| `V5ED0234EC/V5ED234EC` | Mini card processing inactive for logo, DVC ind cannot be 2 or 3 | 
| `V5ED0234EF` | DVC must equal 3 |                                                 
| `V5ED0234EG` | DVC must equal A or D |                                            
| `V5ED0234EH` | DVC must equal C or F |                                            
| `V5ED0234EI` | DVC must equal D |                                                
| `V5ED0234EJ` | DVC must equal F |                                                 
| `V5ED0234EK` | DVC must equal G |                                                 
| `V5ED0237EB` | Cannot have more than one primary card |                           
| `V5ED0240EA/V5ED240EA` | Mobile pi s are not allowed at logo level |                        
| `V5ED0240EB/V5ED240EB` | Mobile pi s are not allowed at account level |                     
| `V5ED0404EB` | Value required for an add |                                        
| `V5ED0407SB` | Org not present in amcr file |                                     
| `V5ED0407SF` | Relationship not present |                                         
| `V5ED0802EA` | Date must be greater than current processing date |                
| `V5ED203EC`  | Nbr requested can not be greater than nbr outstandng |              
| `V5ED204EE`  | Additional card not allowed for smart card |                        
| `V5ED204EF`  | Cannot reissue embosser with status of S |                          
| `V5ED211EA`  | Address line 1 cannot=spaces if city,state,or postal cd not=space | 
| `V5ED221EB`  | Cardholder flag must equal to zeroes for card scheme 0 |            
| `V5ED222EA`  | Value required for an add |                                         
| `V5ED222EB`  | Value is required and cannot equal spaces |                       
| `V5ED4001SD` | Account not present |                                              
| `V5ED4002ED` | Card number must be provided  |                                    
| `V5ED4004SC` | Business unit does not match with input card number |              
| `V5ED4017SA` | Account logo not found |                                           
| `V5ED1901EA` | Group id is not present in group table file |                      
| `V5ED9934EAV5ED9934EB` | Add not allowed, seq nbr would exceed 99 for smart cd |
| `V5AK4003SA` | Card number already exists |                                      
| `V5AK4005SA` | Account number required if card number not provided |             
| `V5AK4011EA` | Embossing card field must be numeric |                            
| `V5AK4012EA` | Embossing req field must be numeric |                              
| `V5AK4024EA` | Pin suppression field must be 0 or 1 |                             
| `V5AK4025EA` | Block code must equal A - Z or space |                             
| `V5AK4043EA` | Next card expire date must be numeric and future date |            
| `V5AK4044EA` | Next card expire date must be numeric and future date |            
| `V5AK4051EA` | Value must be either 1 thru 4 or A thru G |                        
| `V5AK4056SA` | Org/account number combination not found |                         
| `V5AK4061EA` | Number cards required must equal zero or 1 |                       
| `V5AK4063EA` | Embossed name type must not equal 3 |                              
| `V5AK4064EA` | Embossed name 1 must be greater than space |                       
| `V5AK4066EA` | Pin delay days must equal zero for smart card |   
| `V5AK4075EA` | Cardholder flag must equal 0 or 1 for card scheme 2 or 3 |         
| `V5AK4076EA` | Mini field must equal zero for non - visa account |                
| `V5AK4077EA` | Maximum freq input not allowed when no auth limit overrd |         
| `V5AK4087EA` | Next card expire date must be numeric and future date |            
| `V5AK4091EA` | Auth criteria tbl nbr does not match the logo qtrly affl |         
| `V5AK4092EA` | Program id must not be greater than zero for mag strip |           
| `V5AK4097SA` | Card nbr and account nbr must be equal for card scheme |           
| `V5SP4006EA` | Card action should be numeric |                                   
| `V5SP4011SA` | Embosser record not found on file |
| `V5DB4002SA` | AMDB - account not found |                                         
| `V5DB4002SB` | AMDB - account is in add pending |                                 
| `V5DB4001SD` | Customer number can not be spaces |                                
| `V5DB4001AS` | Cust nbr not found |                                               
| `V5DB4001SC` | AMBX rec not found |                                               
| `V5DB4001SE` | AMBS rec not found |                                               
| `V5DB4001SF` | Account not found amax |                                           
| `V5DB4001SH` | AMED record not found |                                            
| `V5DB4001SJ` | ZAMDX rec not found |                                              
| `V5DB4002SA` | AMDB - account not found |                                         
| `V5DB4002SB` | AMDB - account is in add pending |                                 
| `V5DB4001SD` | Customer number can not be spaces |                                
| `V5DB4001AS` | Cust nbr not found |                                               
| `V5DB4001SC` | AMBX rec not found |                                               
| `V5DB4001SE` | AMBS rec not found |                                               
| `V5DB4001SF` | Account not found amax |                                           
| `V5DB4001SH` | AMED record not found |                                            
| `V5DB4001SJ` | ZAMDX rec not found |                                              


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
