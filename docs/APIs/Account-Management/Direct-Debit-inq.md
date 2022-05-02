# Inquire Direct Debit

This service is used to get detail for direct debit for given account. It shows current parameter setup enabled on current account.

## Endpoint

`GET /v1/accounts/{accountNumber}/directDebit`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/directDebit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account number of the cardholder. | 

### Successful Response Payload

```json
{
"accountNumber": "0006000011000000137",
  "billingAcctInd": 0,
  "businessUnit": 600,
  "directDebitDetailsRes": {
    "ddAccountNumber": " ",
    "ddAccountType": "D",
    "ddNominatedPaymentAmtOrPercentage": "10",
    "ddPaymentExpiryDate": "04/12/2022",
    "ddPaymentStartDate": "04/01/2022",
    "ddRoutingBankId": "654321",
    "fixedPaymentAmount": "1",
    "paymentRemittanceMethod": "0"
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0628SV",
  "errorMessage": " Update Request - Record not found "
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |