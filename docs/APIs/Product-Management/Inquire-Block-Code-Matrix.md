# Inquire Block Code Matrix

This API is used to fetch controls defined for each block code at product level.
  
## Endpoint

`GET /v1/products/{productId}/blockCodeMatrix`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Business Unit and product id should be sent as query parameters and path variable.***

<!--
type: tab
-->

```json
{
  "businessUnit": 700,
  "productId": 1,
  "blockCodeControls": [
    {
      "acsBlockCode": 0,
      "authorizationAction": 0,
      "autoBlockCodeAssignment": 0,
      "autoLetterCode1": "B11",
      "autoLetterCode2": "B12",
      "autoLetterCode3": "B13",
      "autoLetterCode4": "B14",
      "autoLetterDays1": 1,
      "autoLetterDays2": 1,
      "autoLetterDays3": 1,
      "autoLetterDays4": 1,
      "description": " ",
      "blockCode": "A",
      "creditBureauStatus": 0,
      "cancelInsuranceIndicator": "N",
      "collectionIndicator": "N",
      "contractualDelinquencyLevel": 0,
      "creditBureauIndicator": "N",
      "defermentsIndicator": "N",
      "waiveFinanceChargeIndicator": "N",
      "frequentShopperIndicator": 0,
      "waiveLateFeeIndicator": "N",
      "waiveMembershipFeeIndicator": 0,
      "waiveNSFChequeFeeIndicator": "N",
      "nextBlockCode": " ",
      "nextBlockMigrationDays": 0,
      "waiveOverlimitFeeIndicator": "N",
      "postingIndicator": 0,
      "priority": 12,
      "recencyDelinquencyLevel": 0,
      "reissueIndicator": "Y",
      "isBlockedAccountReportEnabled": "N",
      "skipPaymentIndicator": 0,
      "statementIndicator": "N",
      "isSuppressLetterEnabled": 0,
      "topUpRedrawIndicator": 0
    }
  ]
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
    "instance": "/v1/products/290/blockCodeMatrix",
    "invalid-params": [
      "V5CR0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productId}/blockCodeMatrix).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Path Variable | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |
| `V5CR0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
