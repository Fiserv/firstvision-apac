# Inquire Account Payoff Quote 

This API is used to fetch calculated payoff amount details for a given accountId.
  
## Endpoint

`GET /v1/accounts/{accountId}/payoffQuote`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000509",
  "businessUnit": 600,
  "cardFeeRebateAmount": "$600.00",
  "currentBalance": "$0.00",
  "financeChargeAmount": "$600.00",
  "payoffQuoteAmount": "$600.00",
  "pendingTransactionAmount": "$600.00",
  "prorataInterestAmount": "$600.00",
  "totalDisputedAmount": "$0.00"
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
    "instance": "/v1/accounts/0007000011001690504/payoffQuote",
    "invalid-params": [
      "V5PQ4001SA: INVALID ORG"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/payoffQuote).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|


### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PQ4001IB` | Adjusted to floor rate 1 |                              
| `V5PQ4001IC` | Used PCT level from Account |                                 
| `V5PQ4001SA` | Invalid Org |                                      
| `V5PQ4001SB` | System Control (AMCR) not found |                                    
| `V5PQ4001SC` | Org not found or is in Add Pending Condition |                     
| `V5PQ4001SD` | System Control PCT Override Lookup Invalid |                        
| `V5PQ4001SE` | System Control PCT Override Lookup Invalid |                        
| `V5PQ4001SF` | Invalid Org |                                                      
| `V5PQ4001SG` | Org Control PCT Override Lookup Invalid |                          
| `V5PQ4001SH` | Org Control PCT Override Lookup Invalid |                           
| `V5PQ4001SI` | Org Control PCT level Not Found |                                   
| `V5PQ4001SJ` | Org Control PCT level Not Found |                                   
| `V5PQ4001SK` | Org Control PCT level Not Found |                                   
| `V5PQ4001SL` | System Control Interest state not found |                           
| `V5PQ4001SM` | Org Control Interest state not found |                              
| `V5PQ4001SN` | Logo Control Interest state not found |                             
| `V5PQ4001SO` | System Control default Interest state not found |                  
| `V5PQ4001SP` | Org Control default Interest state not found |                      
| `V5PQ4001SQ` | Logo Control default Interest state not found |                     
| `V5PQ4001SR` | System Control default Interest state not found |                   
| `V5PQ4001SS` | Org Control default Interest state not found |                      
| `V5PQ4001ST` | Logo Control default Interest state not found |                     
| `V5PQ4001SU` | Interest Rate Table Not Found |                                     
| `V5PQ4001SV` | Usury Table Not Found |                                             
| `V5PQ4001SW` | Default Usury State Of Issue Not Found On Table |                   
| `V5PQ4001SX` | Default Usury State Of Residence Not Found On Table |               
| `V5PQ4001SY` | Rates Are Zero On The State Usury Table |                           
| `V5PQ4002IB` | Adjusted To Floor Rate 2 |                                          
| `V5PQ4002SA` | Invalid Account Or Card Number |                                    
| `V5PQ4002SB` | Account Is Not Active Or Not Found |                                
| `V5PQ4002SC` | Invalid Account Control Table Lookup |                              
| `V5PQ4002SD` | No State Of Issue On The Account |                                  
| `V5PQ4002SE` | No State Of Residence On The Account |                              
| `V5PQ4003IB` | Adjusted To Ceiling Rate 1 |                                        
| `V5PQ4003SA` | Foreign Org Not Found Or Is In Add Pending Condition |             
| `V5PQ4003SF` | Invalid Foreign Use Indicator |                                    
| `V5PQ4004IB` | Adjusted To Ceiling Rate 2 |                                        
| `V5PQ4004SF` | Plan Number Not Numeric |                                           
| `V5PQ4005IB` | Adjusted To Allowable Cap Decrease |                                
| `V5PQ4005SF` | Record Number Not Numeric |                                        
| `V5PQ4006IB` | Adjusted To Allowable Cap Increase |                               
| `V5PQ4006SA` | Logo Control PCT Override Lookup Invalid |                        
| `V5PQ4006SB` | Logo Control PCT Override Lookup Invalid |                         
| `V5PQ4006SC` | Logo Control PCT Override Lookup Invalid |                          
| `V5PQ4006SD` | PCT Override Not Found |                                            
| `V5PQ4007IB` | Making A Usury Adjustment |                                         
| `V5PQ4007SA` | Customer Select Quote Date Not Allowed |                           
| `V5PQ4007SB` | Input Payoff Date Is Invalid |                                     
| `V5PQ4007SC` | Loan Contains A Disputed Amount |                                   
| `V5PQ4007SF` | Payoff By Date Not Numeric |                                        
| `V5PQ4008SA` | Invalid Settlement Type |                                           
| `V5PQ4008SF` | Invalid Settlement Type |                                           
| `V5PQ4009SA` | Credit Plan Record Is Not Found Or Add Pending |                    
| `V5PQ4030SA` | Invalid Plan Number |                                               
| `V5PQ4031SA` | Invalid Plan Sequence |                                            
| `V5PQ4032SA` | Quotes Allowed For Pi1 And Pi2 Loan Plans Only |                    
| `V5PQ4033SA` | Cancel Quote C Invalid As Previous Quote Must Be P W Or C |        
| `V5PQ4034SA` | Quote not allowed as Plan status is 60 |                            
| `V5PQ4035SA` | Quote not allowed as Plan status is 61 |                            
| `V5PQ4036SA` | Quote not allowed as Plan status is 62 |                            
| `V5PQ4037SA` | Quote not allowed as Plan status is 63 |                            
| `V5PQ4038SA` | Quote not allowed as Plan status is 64 |                            
| `V5PQ4039SA` | Quote not allowed as Plan status is 65 |                            
| `V5PQ4040SA` | Quote not allowed as Plan status is 66 |                            
| `V5PQ4041SA` | Quote not allowed as Plan status is 67 |                            
| `V5PQ4042SA` | Quote not allowed as Plan status is 68 |                            
| `V5PQ4043SA` | Quote not allowed as Plan status is 69 |                            
| `V5PQ4044SA` | Quote not allowed as Plan status is 70 |                            
| `V5PQ4045SA` | Quote not allowed as Plan status is 71 |                            
| `V5PQ4046SA` | Quote not allowed as Plan status is 72 |                            
| `V5PQ4047SA` | Quote not allowed as Plan status is 73 |                            
| `V5PQ4048SA` | Quote not allowed as Plan status is 74 |                            
| `V5PQ4049SA` | QUOTE NOT ALLOWED AS PLAN STATUS IS 75 |                            
| `V5PQ4050SA` | Quote not allowed as Plan status is 76 |                            
| `V5PQ4051SA` | Quote not allowed as Plan status is 77 |                            
| `V5PQ4052SA` | Quote not allowed as Plan status is 78 |                            
| `V5PQ4053SA` | Quote not allowed as Plan status is 79 |                            
| `V5PQ4054SA` | Quote not allowed as Plan status is 10 |   

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
