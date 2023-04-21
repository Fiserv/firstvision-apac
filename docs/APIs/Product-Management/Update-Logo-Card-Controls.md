# Update Product Card Controls

This API is used to update card control restriction flags and spend limits for a given product Id. This API can be invoked with a business unit and product Id.

## Endpoint

`PUT /v1/products/{productId}/cardControls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json

{
  "cardControlFields": {
    "maximumAuthorizationLimitFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "$2000.00",
    "maximumAtmCashAuthorizationsCount": 5,
    "maximumSingleAtmTransactionAmount": "$100.00",
    "maximumOtcCashAuthorizationsAmount": "$1500.00",
    "maximumOtcAuthorizationsCount": 6,
    "maximumSingleOtcCashAuthorizationAmount": "$200.00",
    "maximumRetailAuthorizationsAmount": "$100000.00",
    "maximumRetailAuthorizationsCount": 10,
    "maximumSingleRetailAuthorizationAmount": "$10000.00"
  },
  "cardControlFlags": {
    "isAtmEnabled": "Y",
    "isPosEnabled": "Y",
    "isEcomEnabled": "1",
    "isMotoEnabled": "N",
    "isInternationalAtmPosEnabled": "N",
    "isCashBackEnabled": "Y",
    "isPayWaveEnabled": "N"
  },
  "yearToDateCountryRiskSpendLimits": {
    "isCountryRiskSpendLimitEnabled": "1",
    "highRiskCountryMaximumAuthAmount": "$10000.00",
    "otherRiskCountryMaximumAuthAmount": "$15000.00"
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "productId": 1,
  "cardControlFields": {
    "maximumAuthorizationLimitFrequency": "1",
    "maximumAtmCashAuthorizationsAmount": "$2000.00",
    "maximumAtmCashAuthorizationsCount": 5,
    "maximumSingleAtmTransactionAmount": "$100.00",
    "maximumOtcCashAuthorizationsAmount": "$1500.00",
    "maximumOtcAuthorizationsCount": 6,
    "maximumSingleOtcCashAuthorizationAmount": "$200.00",
    "maximumRetailAuthorizationsAmount": "$100000.00",
    "maximumRetailAuthorizationsCount": 10,
    "maximumSingleRetailAuthorizationAmount": "$10000.00"
  },
  "cardControlFlags": {
    "isAtmEnabled": "Y",
    "isPosEnabled": "Y",
    "isEcomEnabled": "1",
    "isMotoEnabled": "N",
    "isInternationalAtmPosEnabled": "N",
    "isCashBackEnabled": "Y",
    "isPayWaveEnabled": "N"
  },
  "yearToDateCountryRiskSpendLimits": {
    "isCountryRiskSpendLimitEnabled": "1",
    "highRiskCountryMaximumAuthAmount": "$10000.00",
    "otherRiskCountryMaximumAuthAmount": "$15000.00"
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
    "instance": "/v1/products/090/cardControls",
    "invalid-params": [
      "V5CR0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/products/{productId}/cardControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Unique identification number associated with the organization. Valid values from 1-998.|
| `productId` | Path Variable | *number* | 03 | Unique identification number of the product associated with the organization. Valid values are 1-998.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |
| `V5CR0010SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
