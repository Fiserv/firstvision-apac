# Update Logo Card Controls

This API is used to perform card control updates at product level. This API can be be invoked with a business unit and product number.

## Endpoint

`PUT /v1/products/{productNumber}/cardControls`

## Payload Example

### Request Payload

```json
{
  "ecomFlag": 1,
  "yearToDateMaxAuthAmountOtherRiskCountry": 15000,
  "otcCashNumber": 6,
  "yearToDateCountryRiskSpendLimitActive": 1,
  "motoFlag": "N",
  "transactionLimitOtc": 200,
  "atmCashNumber": 5,
  "retailPurchaseNumber": 10,
  "transactionLimitAtm": 100,
  "yearToDateMaxAuthAmountHighRiskCountry": 10000,
  "atmFlag": "Y",
  "maximumAuthorizationLimitFrequency": 1,
  "posFlag": "Y",
  "intAtmPosFlag": "N",
  "otcCashAmount": 1500,
  "atmCashAmount": 2000,
  "transactionLimitRetail": 10000,
  "retailPurchaseAmount": 100000
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
  "atmCashAmount": "$20.00",
  "atmCashNumber": 5,
  "atmFlag": "Y",
  "businessUnit": 600,
  "ecomFlag": "1",
  "intAtmPosFlag": "N",
  "maximumAuthorizationLimitFrequency": "1",
  "motoFlag": "N",
  "otcCashAmount": "$15.00",
  "otcCashNumber": 6,
  "posFlag": "Y",
  "productNumber": 1,
  "retailPurchaseAmount": "$1,000.00",
  "retailPurchaseNumber": 10,
  "transactionLimitAtm": "$1.00",
  "transactionLimitOtc": "$2.00",
  "transactionLimitRetail": "$100.00",
  "yearToDateCountryRiskSpendLimitActive": "1",
  "yearToDateMaxAuthAmountHighRiskCountry": "$100.00",
  "yearToDateMaxAuthAmountOtherRiskCountry": "$150.00" 
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