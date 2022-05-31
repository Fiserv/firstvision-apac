# Inquire Direct Debit Controls

This service is used to get detail for direct debit for given account. It shows current parameter setup enabled on current account.

## Endpoint

`GET /v1/accounts/{accountId}/directDebitControls`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/directDebit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Successful Response Payload

```json
{
  "accountId": "0006000011000000137",
  "businessUnit": 600,
  "directDebitDetailsRes": {
    "accountType": "D",
    "externalAccountId": " ",
    "nominatedPaymentAmountPercentage": "10",
    "nominatedType": "1",
    "paymentExpiryDate": "04/12/2022",
    "paymentRemittanceMethod": "0",
    "paymentStartDate": "04/01/2022",
    "routingBankID": "654321"
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0628SV",
  "errorMessage": " Update request - Record not found "
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |