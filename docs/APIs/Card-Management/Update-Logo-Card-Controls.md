# Update Logo Card Controls

This API is used to perform card control updates at product or logo level. This API can be be invoked with an business unit and product number.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/products/{productNumber}/cardControls`

## Payload Example

### Request Payload

```json
{
  "ecomFlag": 1,
  "yeartodateMaxAuthAmountOtherRiskCountry": 15000,
  "otcCashNumber": 6,
  "yeartodateCountryRiskSpendLimitActive": 1,
  "motoFlag": "N",
  "transactionLimitOtc": 200,
  "atmCashNumber": 5,
  "retailPurchaseNumber": 10,
  "transactionLimitAtm": 100,
  "yeartodateMaxAuthAmountHighRiskCountry": 10000,
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

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Identification number associated with this Account Base Segment record, the values are 001–998.|
| `product` | Path Variable | *number* | 03 | This field is the Identification number of the Logo record.|

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
  "yeartodateCountryRiskSpendLimitActive": "1",
  "yeartodateMaxAuthAmountHighRiskCountry": "$100.00",
  "yeartodateMaxAuthAmountOtherRiskCountry": "$150.00" 
}
```

### Error Response Payload

```json
{
   errorCode" :  V5CR0484EA" ,
   errorMessage" : Org Not Found"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org Not Found |
| `V5CR0484EC` | Missing Logo Description Rec |
| `V5CR0484ED` | Add Pending - Logo Desc Rec |