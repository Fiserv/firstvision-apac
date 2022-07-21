# Inquire Service Charge Table

This API retrives various service fee details available in the system for a given Org, Product and table ID combination. The parameters for a Service Charge/Fee table fall into five general categories: penalty fees, periodic fees, service fees, user fees, and prepaid fees etc.

## Endpoint

`GET /v1/products/{productId}/serviceChargeDetails`

## Payload Example

### Request Payload

>Should be empty.
>
>***Business Unit and table id should be sent as query parameters whereas product id as path variable.***
 
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productId}/serviceChargeDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Unique identification number associated with the organization. Valid values from 001-998.|
| `productId` | Path Variable | *number* | 03 | Unique identification number of the product associated with the organization. If the table is defined at organization level, populate this field as zeroes. For tables defined at product level, valid values are 001-998.|
| `tableId` | Query Parameter | *number* | 03 | Identification number of the Service Charge/Fee table. The values are 001–998.|

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "maximumCycleServiceFeeAmount": "$9,999.00",
  "productId": 0,
  "serviceChargeDetails": [
    {
      "dailyFeeDescription": " ",
      "feePlan": "0",
      "feePostingFrequency": "0",
      "feeReverseTransactionCode": 0,
      "initiatingTransactionCode": 3001,
      "maximumIndicator": "0",
      "method": "1",
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "100",
      "tier2Fee": "1000",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
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
      "singleFeeMaximumAmount": 999999999,
      "singleFeeMinimumAmount": 0,
      "tier1Fee": "0",
      "tier2Fee": "0",
      "transactionLimit": 0,
      "transactionLimitFrequency": "0"
    }
  ],
  "tableId": 3
}
```

### Error Response Payload

```json

[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/products/0/serviceChargeDetails",
    "invalid-params": [
      "V5RT0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
Below table provides the list of application's error code and its description.

| `V5PH0004SF` | Get request - Record Not Found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*