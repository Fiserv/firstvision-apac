# Inquire Service Charge Table

This API retrives various service fee details available in the system for a given Org, Product and table ID combination. The parameters for a Service Charge/Fee table fall into five general categories: penalty fees, periodic fees, service fees, user fees, and prepaid fees etc.

## Endpoint

`GET /v1/products/{productNumber}/serviceChargeDetails`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Business Unit and table number should be sent as query parameters whereas product number as path variable.***
 
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productNumber}/serviceChargeDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Identification number of the business unit associated with this Service Charge/Fee table. The values are 000–998.|
| `productNumber` | Path Variable | *number* | 03 | Identification number of the product associated with this Service Charge/Fee table. The values are 000–998.|
| `tableNumber` | Query Parameter | *number* | 03 | Identification number of the Service Charge/Fee table. The values are 001–998.|

### Successful Response Payload

```json

{
  "businessUnit": 600,
  "maximumCycleServiceFees": "$9,999.00",
  "productNumber": 0,
  "serviceChargeDetailsRes": [
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 3001,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "100",
      "tier2ServiceFee": "1000",
      "transactionLimit": 1,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    },
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 0,
      "maximumIndicator": "0",
      "method": "1",
      "serviceFeeMaximumCapping": 999999999,
      "serviceFeeMinimumCapping": 0,
      "tier1ServiceFee": "0",
      "tier2ServiceFee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    }
  ],
  "tableNumber": 3
}

```

### Error Response Payload

```json
{
   errorCode" :  V5PH0004SF" ,
   errorMessage" : Get Request - Record Not Found"   
}
```
Below table provides the list of application's error code and its description.

| `V5PH0004SF` | Get Request - Record Not Found | 