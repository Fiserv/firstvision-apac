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
  "accountId": "0006000011000000509",
  "businessUnit": 600,
  "delinquencyDetails": {
    "120daysDelinquentAmount": "$0.00",
    "150daysDelinquentAmount": "$0.00",
    "180daysDelinquentAmount": "$0.00",
    "210daysDelinquentAmount": "$0.00",
    "30daysDelinquentAmount": "$0.00",
    "60daysDelinquentAmount": "$0.00",
    "90daysDelinquentAmount": "$0.00",
    "currentCycleDue": "0",
    "currentDueAmount": "$0.00",
    "lastDelinquentDate": "00/00/0000",
    "pastDueAmount": "$0.00",
    "paymentDaysDelinquentCount": 0,
    "previousCycleDue": 0
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/deliquencyDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*