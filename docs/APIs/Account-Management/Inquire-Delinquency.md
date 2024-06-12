# Inquire Delinquency

This API is used to fetch delinquency details for a given account Id like 30 to 210 day delinquent amount, last deliquent date, current cycle due etc.

## Endpoint

`GET /v1/accounts/{accountId}/deliquencyDetails`

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
  "accountDetails": {
    "currentBalance": "$0.00",
    "cycleDue": "1",
    "dueDetails": {
      "120daysDelinquentAmount": "$0.00",
      "150daysDelinquentAmount": "$0.00",
      "180daysDelinquentAmount": "$0.00",
      "210daysDelinquentAmount": "$0.00",
      "30daysDelinquentAmount": "$0.00",
      "60daysDelinquentAmount": "$0.00",
      "90daysDelinquentAmount": "$0.00",
      "currentDueAmount": "$10.00",
      "pastDueAmount": "$0.00"
    },
    "openToBuy": "$10000.00",
    "totalDueAmount": "$0.00"
  },
  "accountId": "0007000010000066752",
  "businessUnit": 700,
  "differenceInTotalAmount": "$0.00",
  "planDetails": {
    "currentBalance": "$23.00",
    "planId": 10002,
    "totalDueAmount": "$0.00"
  },
  "planTotalDueAmount": "$20.00",
  "reageDetails": {
    "limit": 1,
    "period": 0,
    "reagedCount": 0
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
    "instance": "/v1/accounts/0006000011000000590/deliquencyDetails",
    "invalid-params": [
      "V5DJ4047SB: Invalid Account Number"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/deliquencyDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5DJ5001SA` | Invalid Organization Entry |
| `V5DJ4047SB` | Invalid Account Number |
| `V5DJ5002SA` | Account Number Required |
| `V5DJ5003SA` | No Organisation Rec on file or Add Pending |
| `V5DJ5004SA` | No Account on file or Add Pending |
| `V5DJ5005SA` | Delinquency Adj not allowed for this Account |
| `V5DJ5006SA` | No Plan Segment(s) on file |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
