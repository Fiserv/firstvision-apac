# Update Insurance

This API is used to update insurance details for a given account Id and insurance product.

## Endpoint

`PUT /v1/insurance/{accountId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "residenceId": "SX1",
  "status": "F",
  "cancelReason": " ",
  "effectiveDate": "10/07/2023",
  "isThirdPartyStatementEnabled": 0,
  "customerId": "0006000012000000256",
  "isThirdPartyLetterFeeEnabled": 1,
  "premiumAmount": "100.00",
  "ficheNumber": "12345",
  "sourceCode": "V1",
  "isThirdPartyLetterEnabled": 0,
  "productParty": 2
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "productId": 1,
  "accountId": "0006000012000000085",
  "recordNumber": 1,
  "insuranceId": "I1",
  "status": "F",
  "residenceId": "SX1",
  "effectiveDate": "10/07/2023",
  "cancelReason": " ",
  "customerId": "0006000012000000256",
  "isThirdPartyStatementEnabled": 0,
  "productPaty": 2,
  "isThirdPartyLetterEnabled": 0,
  "isThirdPartyLetterFeeEnabled": 1,
  "premiumAmount": "$100.00",
  "ficheNumber": "12345",
  "sourceCode": "V1"
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
    "instance": "/v1/insurance/0006000012000000085/details",
    "invalid-params": [
      "V5CR9981SF: Record Not Found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/insurance/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `recordNumber` | Query Parameter | *number* | 2 | Record number associated with insurance product. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR9981SF` | Record not found |
| `V5BS9981SF` | Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
