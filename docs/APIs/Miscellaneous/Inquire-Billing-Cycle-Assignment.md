# Inquire Billing Cycle Assignment

This API is used to fetch billing cycle assignment details and billing method for a given business unit.

## Endpoint

`GET /v1/misc/{businessUnit}/billingCycleAssignment`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Business Unit should be sent as path variable.***


<!--
type: tab
-->

```json

{
  "billingCycleAssignmentDetails": [
    {
      "callCycleNextDay": 1,
      "lastStatementProducedDate": "01/08/2021"
    },
    {
      "callCycleNextDay": 2,
      "lastStatementProducedDate": "02/08/2021"
    },
    {
      "callCycleNextDay": 3,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 4,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 5,
      "lastStatementProducedDate": "05/08/2021"
    },
    {
      "callCycleNextDay": 6,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 7,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 8,
      "lastStatementProducedDate": "08/08/2021"
    },
    {
      "callCycleNextDay": 9,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 10,
      "lastStatementProducedDate": "10/08/2021"
    },
    {
      "callCycleNextDay": 11,
      "lastStatementProducedDate": "11/08/2021"
    },
    {
      "callCycleNextDay": 12,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 13,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 14,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 15,
      "lastStatementProducedDate": "15/08/2021"
    },
    {
      "callCycleNextDay": 16,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 17,
      "lastStatementProducedDate": "17/08/2021"
    },
    {
      "callCycleNextDay": 18,
      "lastStatementProducedDate": "18/08/2021"
    },
    {
      "callCycleNextDay": 19,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 20,
      "lastStatementProducedDate": "20/07/2021"
    },
    {
      "callCycleNextDay": 21,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 22,
      "lastStatementProducedDate": "22/07/2021"
    },
    {
      "callCycleNextDay": 23,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 24,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 25,
      "lastStatementProducedDate": "25/07/2021"
    },
    {
      "callCycleNextDay": 26,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 27,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 28,
      "lastStatementProducedDate": "28/07/2021"
    },
    {
      "callCycleNextDay": 29,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 30,
      "lastStatementProducedDate": "00/00/0000"
    },
    {
      "callCycleNextDay": 31,
      "lastStatementProducedDate": "00/00/0000"
    }
  ],
  "billingMethod": "D",
  "businessUnit": 600
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
    "instance": "/v1/misc/700/billingCycleAssignment",
    "invalid-params": [
      "V5CR0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/misc/{businessUnit}/billingCycleAssignment).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Path Variable | *string* | 3 | Unique identification number associated with the organization. Valid values from 001-998. | 


### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0004SF` | Get request - Record Not Found |
| `V5CR0284EA` | ORG field cannot be zero |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
