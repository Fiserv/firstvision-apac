# Inquire Behavioural History

 This service provides 12 months behavioral history for a given account which include cycle date/balance, cash balance, cash credit limit, payment amount/number, cycle to date late fee/amount, returned number/amount, total amount due, total past due etc.

## Endpoint

`GET /v1/accounts/{accountNumber}/behaviouralHistory`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as and path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/behaviouralHistory).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account. | 

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "accountNumber": "0006000011000000509",
  "behaviouralHistoryDetailsRes": [
    {
      "cycDate": "15/02/2022",
      "cycBalance": "$15000.00",
      "cashBalance": "$0.00",
      "totalCreditLimit": "$20000.00",
      "cashCreditLimit": "$2000.00",
      "amountUsedForPurchases": "$15000.00",
      "numberOfPurchases": 2,
      "cashAmountAdv": "$2000.00",
      "numberOfCashAdvances": 2,
      "balanceTransferAmount": "$0.00",
      "balanceTransferNumber": 0,
      "accessChecksAmount": "$0.00",
      "accessChecksNumber": 0,
      "paymentAmount": "$0.00",
      "paymentNumber": 0,
      "returnedAmount": "$0.00",
      "returnedNumber": 0,
      "nsfCheckAmount": "$0.00",
      "nsfCheckNumber": 0,
      "totalAmountDue": "$0.00",
      "amountPastDue": "$0.00",
      "ctdSvcCharge": "$0.00",
      "ctdLateFeesAmt": "$0.00",
      "ctdLateFeeNumber": 0,
      "ctdOvlmFees": "$0.00",
      "cycleDue": 2,
      "ctdFinanceCharge": "$0.00",
      "userFee1Amount": "$0.00",
      "userFee2Amount": "$0.00",
      "userFee3Amount": "$0.00",
      "userFee4Amount": "$0.00",
      "userFee5Amount": "$0.00",
      "userFee6Amount": "$0.00",
      "tax1Amount": "$0.00",
      "tax2Amount": "$0.00"
    }
  ]
}

```

### Error Response Payload

```json
{
  "errorCode": "V5HB0004SF",
  "errorMessage": "NGet Request - Record Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5HB0004SF` | Get Request - Record Not Found |