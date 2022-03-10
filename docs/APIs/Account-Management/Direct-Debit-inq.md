# Inquire Direct Debit

This service is used to get detail for direct debit for given account. It shows current parameter setup enabled on current account.
Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`GET /v1/accounts/{accountNumber}/directDebit`

## Payload Example

### Request Payload

```json

Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.*** 

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/directDebit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000057",
  "billingAcctInd": "0",
  "businessUnit": "600",
  "ddAccountNumber": " ",
  "ddAccountType": "D",
  "ddNominatedPaymentAmtorPercentage": "10",
  "ddPaymentExpiryDate": "00/00/0000",
  "ddPaymentStartDate": "04/10/2021",
  "ddRoutingBankID": "0",
  "fixedPaymentAmount": "1",
  "paymentRemittanceMethod": "2",
  "product": "600"
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