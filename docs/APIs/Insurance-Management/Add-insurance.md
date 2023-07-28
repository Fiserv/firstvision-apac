# Add Insurance

This API is used to create insurance product for a given account Id along with other details in request.

## Endpoint

`POST /v1/insurance/addInsurance`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "accountId": "0006000011000000103",
  "insuranceId": "I1",
  "status": "F",
  "productParty": 2,
  "ficheNumber": "12345",
  "cancelReason": " ",
  "isThirdPartyStatementEnabled": 0,
  "isThirdPartyLetterFeeEnabled": 1,
  "isThirdPartyLetterEnabled": 0,
  "businessUnit": "600",
  "effectiveDate": "10/07/2023",
  "residenceId": "SX1",
  "customerId": "0006000012000000256",
  "premiumAmount": 0,
  "sourceCode": "V1"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000103",
  "insuranceId": "I1",
  "status": "F"
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "442201",
    "instance": "/v1/insurance/addInsurance",
    "invalid-params": [
      "V5IN4004SB: INSURANCE PRODUCT ALREADY PRESENT FOR THE ACCOUNT"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]
```

<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/insurance/addInsurance).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `insuranceId` | Payload | *string* | 2 | Identification number of the product associated with the account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5IN4001SB` | Org not found |
| `V5IN4002SC` | Account not found or in pending status in AMBS |
| `V5IN4004SD` | INS product not found or in pending status in AMRT |
| `V5IN4004SA` | Invalid product code |
| `V5IN4004SB` | Insurance product already available for the product |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
