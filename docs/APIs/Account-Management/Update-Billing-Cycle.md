# Update Billing Cycle

This API is used to update the billing cycle for an account. Values between 1 to 31 are valid values.

*If user select a nonprocessing day, the cycle’s statement is produced on the processing day that precedes the selected day. This day must be at least 25 calendar days from the **DATE LAST BILLING CYCLE** date. It must also be equal to or greater than the **CURRENT CYCLE** value.*

## Endpoint

`PUT /v1/accounts/{accountId}/billingCycle`

## Payload Example

### Request Payload

```json
{
   "billingCycle": 15
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/billingCycle).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|
| `billingCycle` | payload | *number* | 02 | Cycle code that indicates the day of the month that CMS performs cycle processing for the account. The values are 01–31.|

### Successful Response Payload

```json
{
  "accountId": "0006000011000000111",
  "billingCycle": 15,
  "businessUnit": 600
}
```

### Error Response Payload

```json
{
   errorCode" :  V5BS0010SF" ,
   errorMessage" : Update request - Record not found"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |
| `V5BS0121SA` | Valid entries are 01 Thru 31 |
| `V5BS4001SG` | Org record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*