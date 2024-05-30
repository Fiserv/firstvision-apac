# Update Credit Limit

This API is used to update the credit limit of the cardholder’s account in real time. Newly updated credit limit will be immediately available to use by the cardholder.

## Endpoint

`PUT /v1/accounts/{accountId}/creditLimit`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "creditLimit": "50.00"
}
```

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000152",
  "businessUnit": 600,
  "creditLimit": "$50.00",
  "creditLimitDate": "19/08/2021"
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
    "instance": "/v1/accounts/0006000011000000152/creditLimit",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/creditLimit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |
| `V5BS0103SA` | Credit limit not maintained if relationship level credit limit maintainanace is not allowed |
| `V5BS0103SC` | Input credit limit cannot be greater than logo credit limit |
| `V5BS0103SD` | Credit limit exceeds secured amount use |
| `V5BS0103SE` | Credit limit does not conform to currency NOD |  
| `V5BS0103SF` | Credit limit required |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0103SG` | Cannot be less than logo credit limit |
| `V5BS0103SC` | Cannot be greater than logo credit limit |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
