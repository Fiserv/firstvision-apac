# Inquire Insurance

This API is used to fetch insurance details for a given account Id and insurance product number.

## Endpoint

`GET /v1/insurance/{accountId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id and sequenceNumber should be sent as path variable and query parameter.***

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000012000000085",
  "recordNumber": 1,
  "insuranceId": "I1",
  "description": "DEFAULT INSURANCE TABLE",
  "status": "F",
  "cancelReason": " ",
  "residenceId": "SX1",
  "customerId": "0006000012000000256",
  "isThirdPartyStatementEnabled": 0,
  "isThirdPartyLetterEnabled": 0,
  "isThirdPartyLetterFeeEnabled": 1,
  "productParty": 2,
  "ficheNumber": "12345",
  "sourceCode": "V1",
  "dateFieldDetails": {
    "effectiveDate": "10/07/2023",
    "statusChangeDate": "30/06/2023",
    "cancelDate": "00/00/0000",
    "reinstatementDate": "00/00/0000",
    "birthDate": "00/00/0000",
    "ficheWarnDate": "00/00/0000",
    "ficheCancelDate": "00/00/0000",
    "lastBilledDate": "00/00/0000"
  },
  "premiumDetails": {
    "premiumAmount": "$100.00",
    "rateType": "1",
    "premiumAmountOrPCT": "$0.00",
    "productPremiumAmount": "$0.00"
  },
  "amountDetails": {
    "lastBilledAmount": "$0.00",
    "monthToDateBilledAmount": "$0.00",
    "cycleToDateBilledAmount": "$0.00",
    "yearToDateBilledAmount": "$0.00",
    "lifeToDateBilledAmount": "$0.00",
    "suspendedAmount": "$0.00"
  },
  "productStatusIndicator": "0",
  "sourceCodeDescription": "ABCD",
  "productId": 1
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/insurance/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `recordNumber` | Query Parameter | *number* | 2 | Record number associated with insurance product. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR9981SF` | Record not found |
| `V5BS9981SF` | Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
