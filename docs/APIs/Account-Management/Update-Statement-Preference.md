# Update Statement Preference

This API is used to update statement preferences for a given account Id.

## Endpoint

`PUT /v1/accounts/{accountId}/statementPreferences`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "statementModeOrStatus": "O",
  "statementReprintAddressFlag": "C",
  "ownerCoOwnerStatementFlag": 0
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000145",
  "businessUnit": 600,
  "ownerCoOwnerStatementFlag": 0
  "statementModeOrStatus": "O",
  "statementReprintAddressFlag": "C"
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
    "instance": "/v1/accounts/0006000011000000149/statementPreferences",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/statementPreferences).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |
| `V5BS0122SA` | Valid entries are 0 thru 9, H, O, R, S, U, Or Z |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
