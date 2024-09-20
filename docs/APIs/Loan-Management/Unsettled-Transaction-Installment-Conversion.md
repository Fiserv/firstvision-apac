# Unsettled Transaction Instalment Conversion

This API supports both single and multiple transaction conversion into instalments for a given accountId/paymentInstrumentId. API first validates if given transactions are eligible to convert into instalment. If transactions are eligible, then system converts given transactions into instalment.

## Endpoint

`POST /v1/loans/unsettledTransactionConversion`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "accountId": "0006000011000000509",
  "annualPercentageRate": "0.00000",
  "authorizationCode": "A12352",
  "businessUnit": 600,
  "loanPlanId": 10012,
  "tenure": 12,
  "unsettledTransactionAmount": "1000.00"
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000509",
  "annualPercentageRate": "0.00000%",
  "authorizationCode": "A12345",
  "businessUnit": 600,
  "instalmentDetails": {
    "conversionFeeAmount": "$10.00",
    "instalmentAmount": "$130.00",
    "loanReferenceNumber": "PLAN",
    "planIdDescription": "PLAN",
    "prorataInterestAmount": "$12.00",
    "totalInterestAmount": "$100.00",
    "totalPrincipalAmount": "$1,200.00",
    "totalRepaymentAmount": "$130.00"
  },
  "loanPlanId": 10012,
  "loanScheduleDetails": [
    {
      "conversionFeeAmount": "$5.00",
      "interestAmount": "$12.00",
      "principalAmount": "$1,500.00",
      "tenure": 12,
      "totalBalance": "$1,200.00"
    }
  ],
  "tenure": 12,
  "planSequenceNumber": 1,
  "unsettledTransactionAmount": "$1000.00"
}
```
<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/loans/unsettledTransactionConversion",
    "invalid-params": [
      "V5LU4001EA: ORG NBR MUST BE NUMERIC AND VALID VALUES"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]
```

<!--
 type: tab-end
-->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/loans/unsettledTransactionConversion).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. This API also supports passing the paymentInstrumentId in the accountId in request. When paymentInstrumentId is provided, system identifies the associated accountId. The subsequent processing remain the same as when the accountId is passed.|
| `loanPlanId` | Payload  | *integer* | 05 | Identification number of the Credit Plan Master entity.|
| `tenure` | Payload | *integer* | 03 | Field indicates the term used while converting transaction into instalment.|
| `unsettledTransactionAmount` | Payload | *string* | 17 | Amount of the unsettled transaction.|
| `authorizationCode` | Payload | *string* | 6 | Authorization code assigned to the transaction.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LU4001EA` |Org Nbr Must Be Numeric And Valid Values |                         
| `V5LU4001SF` |Invalid Org |                                                      
| `V5LU4002EA` |Account Number Is Invalid |                                       
| `V5LU4003EA` |Foreign Use Flag Is Invalid |                                      
| `V5LU4003SF` |Invalid Foreign Use Indicator |                                    
| `V5LU4004EA` |Credit Limit Function Must Be I Or D |                             
| `V5LU4004SF` |Invalid Function Code |                                            
| `V5LU4005EA` |Temp Credit Limit Option Must Be 0 1 Space Or Low Value |          
| `V5LU4005SF` |Invalid Credit Limit Option |                                      
| `V5LU4006EA` |Triad Action Must Be A O Or R |                                   
| `V5LU4006SF` |Invalid Action Code |                                              
| `V5LU4007EA` |Traid Offer Amount Must Be Numeric |                               
| `V5LU4007SF` |Credit Limit Not Numeric |                                         
| `V5LU4008EA` |Credit Limit Must Be Numeric |                                     
| `V5LU4008SF` |Credit Limit Triad Not Numeric |                                   
| `V5LU4009EA` |Triad Override Credit Limit Must Be Numeric |                      
| `V5LU4009SF` |Override Credit Limit Not Numeric |                                
| `V5LU4010EA` |Org Not Found On File |                                            
| `V5LU4011EA` |Foreign Org Not Found On File |                                   
| `V5LU4012EA` |Account Number Not Found |                                         
| `V5LU4013EA` |Logo Not Found On File |                                           
| `V5LU4014EA` |Servere Error No Cust Service Rep Assign To Operator |             
| `V5LU4015EA` |Servere Error No Cust Service Rep Assign To Operator |             
| `V5LU4016EA` |Perm Cr Lim Cant Change Temp Cr Limit Is In Effect |               
| `V5LU4017EA` |Traid Cred Lim Offer Must Be Num When Triad Active |               
| `V5LU4018EA` |Traid Action Code Must Be A O Or R When Traid Active |             
| `V5LU4019EA` |Override Amt Must Be Num When Action Code O |                      
| `V5LU4020EA` |Override Amt Must Be Greater Than Existing Cr Limit Increase Func |
| `V5LU4022EA` |Override Amt Must Be Greater Than Existing Crlim Increase Func |   
| `V5LU4023EA` |Override Amt Must Be Less Than Existing Crlim Decrease Function |  
| `V5LU4024EA` |Traid Ofr Amt Must Be Num When Action Code Is A |                  
| `V5LU4025EA` |Traid Ofr Amt Must Be Greater Than Existing Crlim Increase Func |  
| `V5LU4026EA` |Traid Ofr Amt Must Be Less Than Existing Crlim On Decrease Func |  
| `V5LU4027EA` |Traid Ofr Amt Must Be Greater Than Existing Crlim On Increas Func |
| `V5LU4028EA` |Traid Ofr Amt Must Be Less Than Existing Crlim On Decrease Func |  
| `V5LU4029EA` |Credit Limit Must Be Numeric |                                     
| `V5LU4030EA` |New Crlim Must Be Greater Than Existing Crlim On Increase Func |   
| `V5LU4031EA` |New Crlim Must Be Less Than Existing Crlim On Decrease Function |  
| `V5LU4032EA` |New Crlim Must Be Greater Than Existing Crlim On Increase Func |   
| `V5LU4033EA` |New Crlim Must Be Less Than Existing Crlim On Decrease Function |  
| `V5LU4034EA` |Override Credit Limit Exceeds Logo Ceiling Limit |                 
| `V5LU4035EA` |Traid Credit Limit Exceeds Logo Ceiling Limit | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
