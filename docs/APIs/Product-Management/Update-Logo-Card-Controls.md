# Update Logo Card Controls

This API is used to perform card control updates at product level. This API can be be invoked with a business unit and product number.

## Endpoint

`PUT /v1/products/{productNumber}/cardControls`

## Payload Example

### Request Payload

```json
{
  "cardControlFieldsReq": {
    "maximumAuthorizationLimitFrequency": "1",
    "atmCashAmount": "2000.0",
    "atmCashNumber": 5,
    "transactionLimitAtm": "100.0",
    "otcCashAmount": "1500.0",
    "otcCashNumber": 6,
    "transactionLimitOtc": "200.0",
    "retailPurchaseAmount": "100000.0",
    "retailPurchaseNumber": 10,
    "transactionLimitRetail": "10000.0"
  },
  "cardControlFlagsReq": {
    "atmFlag": "Y",
    "posFlag": "Y",
    "ecomFlag": "1",
    "motoFlag": "N",
    "intAtmPosFlag": "N"
  },
  "yearToDateCountryRiskSpendLimitsReq": {
    "yearToDateCountryRiskSpendLimitActive": "1",
    "yearToDateMaxAuthAmountHighRiskCountry": "10000.0",
    "yearToDateMaxAuthAmountOtherRiskCountry": "15000.0"
  }
}

``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/products/{productNumber}/cardControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Identification number associated with this Account Base Segment record, the values are 001–998.|
| `product` | Path Variable | *number* | 03 | This field is the identification number of the Logo record.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "cardControlFieldsRes": {
    "atmCashAmount": "$200.00",
    "atmCashNumber": 5,
    "maximumAuthorizationLimitFrequency": "1",
    "otcCashAmount": "$150.00",
    "otcCashNumber": 6,
    "retailPurchaseAmount": "$10,000.00",
    "retailPurchaseNumber": 10,
    "transactionLimitAtm": "$10.00",
    "transactionLimitOtc": "$20.00",
    "transactionLimitRetail": "$1,000.00"
  },
  "cardControlFlagsRes": {
    "atmFlag": "Y",
    "ecomFlag": "1",
    "intAtmPosFlag": "N",
    "motoFlag": "N",
    "posFlag": "Y"
  },
  "productNumber": 1,
  "yearToDateCountryRiskSpendLimitsRes": {
    "yearToDateCountryRiskSpendLimitActive": "1",
    "yearToDateMaxAuthAmountHighRiskCountry": "$1,000.00",
    "yearToDateMaxAuthAmountOtherRiskCountry": "$1,500.00"
  }
}

```

### Error Response Payload

```json
{
   errorCode" :  V5CR0484EA" ,
   errorMessage" : Org not found"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |
| `V5CR0010SF` | Update Request - Record not found |