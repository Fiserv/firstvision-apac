# Update Delinquency

This service is used to reage the account, reaging an account is normally done to cause an account to appear less delinquent by reducing the delinquency level. You also can reage an account to make the account appear more delinquent by increasing the delinquency level.

## Endpoint

`PUT /v1/accounts/{accountId}/updateDelinquency`

## Payload Example

### Request Payload

```json
{
  "cycleDue": "1",
  "accountDues": {
    "currentDueAmount": "$0.00",
    "pastDueAmount": "$0.00",
    "30daysDelinquentAmount": "$0.00",
    "60daysDelinquentAmount": "$0.00",
    "90daysDelinquentAmount": "$0.00",
    "120daysDelinquentAmount": "$0.00",
    "150daysDelinquentAmount": "$0.00",
    "180daysDelinquentAmount": "$0.00",
    "210daysDelinquentAmount": "$0.00"
  },
  "totalPlanDueAmount": "$0.00",
  "planDues": [
    {
      "planId": 10002,
      "totalDueAmount": "$0.00"
    }
  ]
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/updateDelinquency).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "accountDues": {
    "120daysDelinquentAmount": "$0.00",
    "150daysDelinquentAmount": "$0.00",
    "180daysDelinquentAmount": "$0.00",
    "210daysDelinquentAmount": "$0.00",
    "30daysDelinquentAmount": "$0.00",
    "60daysDelinquentAmount": "$0.00",
    "90daysDelinquentAmount": "$0.00",
    "currentDueAmount": "$0.00",
    "pastDueAmount": "$0.00"
  },
  "accountId": "0001000010000028800",
  "businessUnit": 100,
  "differenceInTotalAmount": "$0.00",
  "planDues": [],
  "reageCycleDue": "1",
  "totalPlanDueAmount": "$0.00"
}
```

### Error Response Payload

```json
{
   "errorCode" :  "V5D24201SA" ,
   "errorMessage" : "Reage cycle due flag is not valid"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS9981SF` | Record not found |
| `V5D24201SA` | Reage cycle due flag is not valid |
| `V5D24209SA` | Error processing current balance |
| `V5D24207SA` | Reage CD flag not valid on this plan |
| `V5D24205SA` | Plan is deferred and total due not zeroes |
| `V5D24203SA` | Curr due field entered - Reage CD not allowed |
| `V5D24206SA` | Calculated balance is greater than curr bal |
| `V5D24210SA` | Total plan balance does not match with base segment bal |
| `V5D24208SA` | Computed bal is more than base sgmt bal & diff in total is 00000000000000000 |
