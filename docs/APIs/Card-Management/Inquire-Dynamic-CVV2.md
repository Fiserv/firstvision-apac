# Inquire Dynamic CVV2

This API is used to fetch encrypted dynamic CVV2 provide other additional details like encrypted payment card number, encrypted expiry date, embossed name 1, embossed name 2, dynamic CVV2 expire date and time for a given payment instrument Id.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/dynamicCVV2`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***The Payment Instrument Identification should be sent as path variable.***

<!--
type: tab
--> 

```json
{
  "encryptedPaymentCardNumber": "217E8A00536C7A101B055563FBF49C9A",
  "encryptedDynamicCVV2": "C8FB47CB632D1D16",
  "encryptedCardExpiryDate": "6D259F94D6096444",
  "embossedName1": "John Brono ",
  "embossedName2": "Samuel Baro",
  "dynamicCVV2ExpiryDateTime": "27/07/2022 16:00:23"
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
    "instance": "/v1/cards/0009846801010065781/dynamicCVV2",
    "invalid-params": [
      "V5DI4002SB: ACCT IS PURGED/FRAUD/CLOSED/CGOFF OR ADD PENDING/NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/dynamicCVV2).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |


### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
| `V5DI4002SB` | Acct is purged/fraud/closed/cgoff or add pending/not found |
| `V5DI4002SV/V5DI4002SA` | Card number should be numeric and not zeroes |  
| `V5DI4004SV` | Valid values are Y and N for disable DCCV2 method flag |    
| `V5DI4001SA` | Invalid card/org |                                               
| `V5DI4001SB` | Org security failed |  
| `V5DI4002SC` | Acct is billing/control/diversion acct |                          
| `V5DI4002SD` | Acct warning code is 1/2/3/4/8 |                                 
| `V5DI4002SE` | Card is add pending/purged/fraud/notfnd |                       
| `V5DI4002SF` | Card warning code is 1/2/3/4/8 |                                 
| `V5DI4002SG` | Card not active |                                                
| `V5DI4002SH` | Card got expired |                              
| `V5DI4002SJ` | Not valid visa affiliation |                                     
| `V5DI4002SK` | DCVV2 method is static at logo level |                           
| `V5DI4002SL` | HSM call failed |                                                 
| `V5DI4002SM` | DCVV2 method is static at global parm level |                    
| `V5DI4002SN` | DCVV2 not generated yet |                          
| `V5DI4001SE` | ZEK PAN encryption failed |                                       
| `V5DI4001SF` | ZEK DCVV2 encryption failed |                                    
| `V5DI4001SG` | ZEK MM/YY encryption failed |                                    
| `V5DI4001IA` | Static CVV2 is set for this card successfully |                  
| `V5DI4001IB` | Dynamic CVV2 activated and DCVV2 generated successfully |        
| `V5DI4003SB` | Key system file not found |                                      
| `V5DI4003SC` | Key system record read fail |                                   
| `V5DI4003SD` | Key file record not found |                                      
| `V5DI4003SE` | Key file record read fail |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
