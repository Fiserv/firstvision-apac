# Inquire Maximum Eligible Transaction Amount

This API will be called to get the maximum eligible transaction amount for TIP loans for a given Account and Promo Plan provided in the input. 

## Endpoint

`GET /v1/loans/{accountId}/maximumEligibleTransactionAmount`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id and loanPlanId should be sent as path variable and query parameter respectively.***

<!--
type: tab
-->

```json
{
	"maximumEligibleBalanceForTransactionInstalment": "$500.00",
	"loanPlanId": 55001,
	"accountId": "0007000022274307502",
	"businessUnit": 700
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
    "instance": "/v1/loans/0007001000001035405/maximumEligibleTransactionAmount",
    "invalid-params": [
      "V5LB4002EB: Account / Card number is not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/maximumEligibleTransactionAmount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `loanPlanId` | Payload  | *integer* | 05 | Identification number of the Credit Plan Master entity.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LB4001EA` | Business unit is not determined |                                  
| `V5LB4002EA` | Account / Card number is required |                                
| `V5LB4003EA` | Promo plan is required |                                           
| `V5LB4001EB` | Business unit is not present in file |                             
| `V5LB4002EB` | Account / Card number is not found |                               
| `V5LB4003EB` | Plan record not found on plan segment file |                                          
| `V5LB4003EC` | Invalid loan plan type | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
