# List Plans

This API is used to fetch list of plans and its details for a given account Id.

## Endpoint

`GET /v1/accounts/{accountId}/planList`

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
  "planDetails": [
    {
      "accountId": "0006000011000000137",
      "accruedThroughDate": "18/08/2021",
      "addedDate": "17/08/2021",
      "annualFeeBilledNotPaidAmount": "$50.00",
      "billingBeginningDate": " ",
      "businessUnit": 600,
      "collectionFeeBilledNotPaidAmount": "$0.00",
      "currentBalance": "$70.00",
      "description": "RETAIL PLAN",
      "disputedAmount": "$0.00",
      "insuranceBilledNotPaidAmount": "$0.00",
      "interestBilledNotPaidAmount": "$0.00",
      "lateFeeBilledNotPaidAmount": "$0.00",
      "nsfFeeBilledNotPaidAmount": "$0.00",
      "overlimitFeeBilledNotPaidAmount": "$0.00",
      "paymentBeginningDate": " ",
      "planId": 10002,
      "principalAmount": "$20.00",
      "rateType": "F",
      "planSequenceNumber": 1,
      "recoveryFeeBilledNotPaidAmount": "$0.00",
      "serviceFeeBilledNotPaidAmount": "$0.00",
      "status": "1"
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
    "instance": "/v1/accounts/000600001100000013A/planList",
    "invalid-params": [
      "V5PS4002SF: INVALID ACCOUNT"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/planList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PS4002SF` | Invalid account |
| `V5PS4010SA` | Account not present in account file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
