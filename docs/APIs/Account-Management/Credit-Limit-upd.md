# Update Credit Limit

This service is used to update the credit limit of the cardholder’s account in real time. Newly updated credit limit will be available to use Immediately to the cardholder.

## Endpoint

`PUT /v1/accounts/{accountNumber}/creditLimit`

## Payload Example

### Request Payload

```json
{
  "creditLimit": 50   
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/creditLimit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `creditLimit` | Payload | *string* | 17 | Credit limit of the account. |

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000103",
  "businessUnit": "600",
  "creditLimit": "$10.00",
  "creditLimitDate": "19/08/2021"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0010SF",
  "errorMessage": " Update Request - Record not found "
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0103SA` | Credit limit not maintained if relationship level credit limit maintainanace is not allowed |
| `V5BS0103SC` | Input credit limit cannot be greater than logo credit limit |
| `V5BS0103SD` | Credit limit exceeds secured amount use |
| `V5BS0103SE` | Credit limit does not conform to currency NOD |  
| `V5BS0103SF` | Credit limit required |
| `V5BS0010SF` | Update Request - Record not found |