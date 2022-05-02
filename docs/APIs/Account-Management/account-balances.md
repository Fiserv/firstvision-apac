# Inquire Account Balances

The service provide account's balances such as available balance/ current balance / due amount / last payment amount / first purchase amount / credit limit, associated with the customer.

## Endpoint

`GET /v1/accounts/{accountNumber}/balances`

## Payload Example

### Request Payload

>Shoud be empty.
>
>***The Account Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/balances).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000343",
  "amountMemoCredit": "$0.00",
  "amountMemoDebit": "$0.00",
  "billingCycle": 18,
  "blockCode1": "",
  "blockCode2": "",
  "blockCodeDate1": "00/00/0000",
  "blockCodeDate2": "00/00/0000",
  "businessUnit": 600,
  "cashAvailable": "$0.00",
  "cashBalance": "$0.00",
  "cashCreditLimit": "$0.00",
  "chargeOffStatus": "0",
  "creditLimit": "$10,000.00",
  "currentBalance": "$0.00",
  "currentDue": "$0.00",
  "customerNumber": "0000000001000000003",
  "cycleToDatePayment": "$0.00",
  "dateAccountOpened": "19/08/2021",
  "dateFirstPurchase": "00/00/0000",
  "dateLastPayment": "00/00/0000",
  "dateLastStatement": "00/00/0000",
  "dateOfLastPurchase": "00/00/0000",
  "firstPurchaseAmount": "$0.00",
  "graceDayExpireDate": "00/00/0000",
  "internalStatus": "N",
  "lastPaymentAmount": "$0.00",
  "loanAvailable": "$0.00",
  "loanBalance": "$0.00",
  "loanCreditLimit": "$0.00",
  "nextStatementDate": "00/00/0000",
  "openToBuy": "$0.00",
  "pastDuePaymentAmount": "$0.00",
  "paymentDueDate": "00/00/0000",
  "shortName": "",
  "totAmtDue": "$0.00"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0004SF",
  "errorMessage": "Get Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get Request - Record not found|
