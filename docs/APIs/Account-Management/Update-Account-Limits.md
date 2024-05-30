# Update Account Limits

This API allows user to set daily maximum cash deposit authorization amount and count for a given accountId. 

## Endpoint

`PUT /v1/accounts/{accountId}/limits`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "cashDepositLimits": {
    "maximumAuthorizationAmount": "1000.00",
    "maximumAuthorizationCount": 5
  }
}
```

<!--
type: tab
-->

```json
{
  "cashDepositLimits" : {
    "maximumAuthorizationAmount" : "$1,000.00",
    "maximumAuthorizationCount" : 5
  },
  "businessUnit" : 700,
  "accountId" : "0007001000001035405"
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
    "instance": "/v1/accounts/0007001000001035405/limits",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/limits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountid` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
