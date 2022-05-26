# Inquire Plan Master

This service provides plan details for a given credit plan. Credit plans are control records that will be defined at the Business Unit level. Credit plans are defined to specify the various methods that are being offered to the customer. It will contain information like description, interest table override options, cancellation or expiry parameters based on account's performace etc.
  
## Endpoint

`GET /v1/products/{planId}/planDetails`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Business Unit and Plan id should be sent as query parameters and path variable.*** 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{planId}/planDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number associated with this Account Base Segment record, the values are 001–998. |
| `planId` | Path Variable | *number* | 5 | Identification number of the Credit Plan Master record. The values are 00001–99998. You can establish as many as 99,998 Credit Plan Master records for each organization. | 

### Successful Response Payload

```json

{
  "businessUnit": 600,
  "planId": 10002,
  "description": "RETAIL PLAN",
  "planType": "R",
  "multipleSales": "Y",
  "paymentType": "T",
  "balanceTransferType": "N",
  "graceBalanceQualification": "1",
  "interestRateTableId": "1",
  "interestRateTableOverrideRes": {
    "tableId": 1,
    "expiryDate": "15/08/2023"
  },
  "consolidatedDetailsRes": {
    "controllingCreditPlanMaster": 10003,
    "isConsolidatedStatement": "Y",
    "consolidatedPayment": "Y"
  },
  "promotionalPlanDetailsRes": {
    "latePaymentCancelRoll": "1",
    "delinquencyLevelToCancel": "6",
    "cancellationLetterId": "",
    "cancellationRollOverPlanId": 50002,
    "cancellationPlanRollOverMethod": "0",
    "expirationRollover": "1",
    "expirationLetter": "EXP",
    "expirationRollOverPlanId": 50001,
    "expirationPlanRollOverMethod": "0"
  }
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