# List Transaction Instalments

This API is used to fetch details of all transaction instalment loans against an account.

## Endpoint

`GET /v1/loans/{accountId}/listTransactionInstalments`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable.***

<!--
type: tab
-->

```json
{
    "instalmentDetails": [
        {
            "loanReferenceNumber": "202409300003",
            "loanStatus": "A"
        }
    ],
    "conversionDate": "10/10/2023",
    "accountId": "0007000011000000608",
    "businessUnit": 700,
    "totalInstalmentCount": 1
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
    "instance": "/v1/loans/0007000011000000608/listTransactionInstalments",
    "invalid-params": [
      "V5LG4002EB: Account / card number is not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/listTransactionInstalments).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5LG4001EA` | Business unit is not determined |  
| `V5LG4001EB` | Business unit is not present in file |  
| `V5LG4002EA` | Account / card number is required |
| `V5LG4003EA` | Conversion date should not be greater than todays date |
| `V5LG4002EB` | Account / card number is not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
