# Update Temporary Credit Limit

This service is used to update temporary credit limit to an account. This service can be called with an account number to update the *temporary credit limit* of the account. This service will require the account number, Temporary credit limit and its limit expiry date in the input message.

## Endpoint

`PUT /v1/accounts/{accountId}/tempCreditLimit`

## Payload Example

### Request Payload

```json
{
  "temporaryCreditLimit": "$1000.00",
  "temporaryCreditLimitExpiryDate": "31/10/2022"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/tempCreditLimit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "accountId": "0006000011000000103",
  "businessUnit": 600,
  "creditLimit": "$1,000.00",
  "temporaryCreditLimit": "$0.00",
  "temporaryCreditLimitExpiryDate": "31/10/2022"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000101/tempCreditLimit",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0601EA` | Temp credit limit does not conform to currency NOD |
| `V5BS0601EB` | Temp credit limit field not editable when debit active at logo |
| `V5BS0601EC` | Temp credit limit cannot be greater than logo credit limit |
| `V5BS0601ED` | Temp credit limit is not maintained if relationship level credit limit maintenance is not allowed |
| `V5BS0601SB` | Temp credit limit whole monetary unit-does not conform to currency NOD |
| `V5BS0601SC` | Temp credit limit cannot be greater than logo credit limit |
| `V5BS0601EE` | Temp credit limit can't be updated for prepaid account |
| `V5BS0601EF` | Temp credit limit can't be updated for prepaid account |
| `V5BS0602EA` | Temp credit limit exp must be greater than cms file date |
| `V5BS0602EB` | Temp credit limit exp must be equal or greater than cms file date |
| `V5BS0602EC` | Temp credit limit and expiry date conflicts |
| `V5BS0602ED` | Temp credit limit expires today. expiry dte must be > cms file date |
| `V5BS0602EE` | Verify temp credit line and press enter if correct |
| `V5BS0602EF` | Temp credit limit exp not editable when debit active at logo |
| `V5BS0602EG` | Temp expires today.update the temp expiry date |
| `V5BS0602EH` | Credit limit and expiry date cannot be zeroed out |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*