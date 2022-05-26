# Update Product Card Controls

This API is used to perform card control updates at product level. This API can be be invoked with a business unit and product number.

## Endpoint

`PUT /v1/products/{productId}/cardControls`

## Payload Example

### Request Payload

```json

{
  "cardControlFieldsReq": {
    "maximumAuthorizationLimitFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "2000.0",
    "maximumAtmCashAuthorizationsCount": 5,
    "maximumSingleAtmTransactionAmount": "100.0",
    "maximumOtcCashAuthorizationsAmount": "1500.0",
    "maximumOtcAuthorizationsCount": 6,
    "maximumSingleOtcCashAuthorizationAmount": "200.0",
    "maximumRetailAuthorizationsAmount": "100000.0",
    "maximumRetailAuthorizationsCount": 10,
    "maximumSingleRetailAuthorizationAmount": "10000.0"
  },
  "cardControlFlagsReq": {
    "isAtmEnabled": "Y",
    "isPosEnabled": "Y",
    "isEcomEnabled": "1",
    "isMotoEnabled": "N",
    "isInternationalAtmPosEnabled": "N",
    "isCashBackEnabled": "Y",
    "isPayWaveEnabled": "N"
  },
  "yearToDateCountryRiskSpendLimitsReq": {
    "isCountryRiskSpendLimitEnabled": "1",
    "highRiskCountryMaximumAuthAmount": "10000.0",
    "otherRiskCountryMaximumAuthAmount": "15000.0"
  }
}

``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/products/{productId}/cardControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Unique identification number associated with the organization. Valid values from 001-998.|
| `productId` | Path Variable | *number* | 03 | Unique identification number of the product associated with the organization. Valid values are 001-998..|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json

{
  "businessUnit": 600,
  "productId": 1,
  "cardControlFieldsRes": {
    "maximumAuthorizationLimitFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "2000.0",
    "maximumAtmCashAuthorizationsCount": 5,
    "maximumSingleAtmTransactionAmount": "100.0",
    "maximumOtcCashAuthorizationsAmount": "1500.0",
    "maximumOtcAuthorizationsCount": 6,
    "maximumSingleOtcCashAuthorizationAmount": "200.0",
    "maximumRetailAuthorizationsAmount": "100000.0",
    "maximumRetailAuthorizationsCount": 10,
    "maximumSingleRetailAuthorizationAmount": "10000.0"
  },
  "cardControlFlagsRes": {
    "isAtmEnabled": "Y",
    "isPosEnabled": "Y",
    "isEcomEnabled": "1",
    "isMotoEnabled": "N",
    "isInternationalAtmPosEnabled": "N",
    "isCashBackEnabled": "Y",
    "isPayWaveEnabled": "N"
  },
  "yearToDateCountryRiskSpendLimitsRes": {
    "isCountryRiskSpendLimitEnabled": "1",
    "highRiskCountryMaximumAuthAmount": "10000.0",
    "otherRiskCountryMaximumAuthAmount": "15000.0"
  }
}

```

### Error Response Payload

```json
{
   "errorCode" :  "V5CR0484EA" ,
   "errorMessage" : "Org not found"
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |
| `V5CR0010SF` | Update Request - Record not found |