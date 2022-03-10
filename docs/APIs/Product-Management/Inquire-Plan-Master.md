# Inquire Plan Master

This service provides plan details for a given credit plan. Credit plans are control records that will be defined at the Business Unit level. Credit plans are defined to specify the various methods that are being offered to the customer. It will contain information like description, interest table override options, cancellation or expiry parameters based on account's performace etc
  
## Endpoint

`GET /v1/products/{planNumber}/planDetails`

## Payload Example

### Request Payload

```json
Shoud be empty.
***The Business Unit and Plan Number should be sent as query parameters and path variable.*** 
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](..api/?type=get&path=/v1/products/{planNumber}/planDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Business Unit - Identification number associated with this Account Base Segment record, the values are 001–998 |
| `planNumber` | Path Variable | *number* | 5 | Plan Number - Identification number of the Credit Plan Master record. The values are 00001–99998. You can establish as many as 99,998 Credit Plan Master records for each organization | 

### Successful Response Payload

```json
{
  "balanceTransferType": "N",
  "businessUnit": 600,
  "cancellationLetterId": "",
  "cancelledPlanRollMethod": "0",
  "consolidatedPayment": "Y",
  "consolidatedStatement": "Y",
  "controllingCreditPlanMaster": 10002,
  "delinquencyLevelToCancel": "0",
  "expirationLetter": "",
  "expirationRollover": "0",
  "expiredPlanRollMethod": "0",
  "graceBalanceQualification": "0",
  "interestRateTableId": "2",
  "interestRateTableOverride": 0,
  "itoExpirationDate": "00/00/0000",
  "latePaymentCancelRoll": "0",
  "minimumPaymentCalculation": "T",
  "multipleSales": "Y",
  "planNumber": 10002,
  "planType": "R",
  "rollCancelledPlanToPlanId": 0,
  "rollExpiredPlanToPlanId": 0
}
```

### Error Response Payload

```json
{
  "errorCode": "V5CP0004SF",
  "errorMessage": "Get Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CP0004SF` | Get Request - Record not found |         