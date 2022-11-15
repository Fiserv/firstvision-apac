# Inquire Plan Master

This service provides plan details for a given credit plan. Credit plans are control entities that will be defined at the Business Unit level. Credit plans are defined to specify the various methods that are being offered to the customer. It will contain information like description, interest table override options, cancellation or expiry parameters based on account's performace etc.
  
## Endpoint

`GET /v1/products/{planId}/planDetails`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Business Unit and Plan id should be sent as query parameters and path variable.*** 

<!--
type: tab
--> 

```json
{
  "balanceTransferType": "N",
  "businessUnit": 600,
  "consolidatedDetails": {
    "consolidatedPayment": "Y",
    "controllingCreditPlanMaster": 10002,
    "isConsolidatedStatementEnabled": "Y"
  },
  "description": "RETAIL PLAN",
  "graceBalanceQualification": "0",
  "interestRateTableId": "2",
  "interestRateTableOverride": {
    "expiryDate": "00/00/0000",
    "tableId": 0
  },
  "multipleSales": "Y",
  "paymentType": "T",
  "planId": 10002,
  "planType": "R",
  "promotionalPlanDetails": {
    "cancellationLetterId": "",
    "cancellationPlanRollOverMethod": "0",
    "cancellationRollOverPlanId": 0,
    "delinquencyLevelToCancel": "0",
    "expirationLetter": "",
    "expirationPlanRollOverMethod": "0",
    "expirationRollOverPlanId": 0,
    "expirationRollover": "0",
    "latePaymentCancelRoll": "0"
  }
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
    "instance": "/v1/products/10009/planDetails",
    "invalid-params": [
      "V5CP0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{planId}/planDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number associated with this Account Base Segment entity, the values are 001–998. |
| `planId` | Path Variable | *number* | 5 | Identification number of the Credit Plan Master entity. The values are 00001–99998. You can establish as many as 99,998 Credit Plan Master entities for each organization. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CP0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*