# Inquire Account Preference

This API is used to fetch the details like statement preferences, various customer IDs, address ID, source code, suppress token indicator for a given account Id. 

## Endpoint

`GET /v1/accounts/{accountId}/preference`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "accountId": "0004440010000000017",
  "addressId": "",
  "alternateCustomerIdDetails": {
    "customerId": "0000000001000000065",
    "customerIdEffectiveDate": "14/01/2021",
    "customerIdExpiryDate": "15/05/2022",
    "customerIdFlag": "A"
  },
  "businessUnit": 600,
  "correspondenceCustomerId": "0000000001000000065",
  "customerId": "0000000001000000032",
  "isSupressTokenEnabled": 0,
  "sourceCode": "",
  "statementPreferenceDetails": {
    "ownerCoOwnerStatementFlag": "0",
    "statementModeOrStatus": "O",
    "statementReprintAddressFlag": "C",
    "statementDeliveryMode": "E"
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
    "instance": "/v1/accounts/0004440010000000016/preference",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/preference).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found|

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*