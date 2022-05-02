# List Of Plan Segment

This service is used to retrieve list of plans on account. Along with list of plans it shows the summary of plan level activities.

## Endpoint

`GET /v1/accounts/{accountNumber}/planList`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Account Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/planList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the account.|

### Successful Response Payload

```json

{
  "planDetailsRes": [
    {
      "accountNumber": "0006000011000000137",
      "accruedThroughDate": "18/08/2021",
      "annualFeeBilledNotPaidAmount": "$50.00",
      "billingBeginningDate": "",
      "businessUnit": 600,
      "collectionFeesBilledNotPaidAmount": "$0.00",
      "currentBalance": "$70.00",
      "dateAdded": "17/08/2021",
      "disputedAmount": "$0.00",
      "insuranceBilledNotPaidAmount": "$0.00",
      "interestBilledNotPaidAmount": "$0.00",
      "lateChargeBilledNotPaidAmount": "$0.00",
      "nsfBilledNotPaidAmount": "$0.00",
      "overlimitFeeBilledNotPaidAmount": "$0.00",
      "paymentBeginningDate": "",
      "planDescription": "RETAIL PLAN",
      "planNumber": 10002,
      "planStatus": "61",
      "principalBalance": "$20.00",
      "rateType": "F",
      "recoveryFeesBilledNotPaidAmount": "$0.00",
      "serviceChargeBilledNotPaidAmount": "$0.00"
    }
  ]
}

```

### Error Response Payload

```json
{
   errorCode" :  V5PS4010SA" ,
   errorMessage" : Account not present in account file"   
}
```
Below table provides the list of application's error code and its description.

| `V5PS4010SA` | Account not present in account file | 