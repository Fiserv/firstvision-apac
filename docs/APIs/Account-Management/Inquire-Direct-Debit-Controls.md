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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/directDebitControls).


The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Successful Response Payload

```json
{
  "accountId": "0006000011000000137",
  "accountType": "D",
  "businessUnit": 600,
  "externalAccountId": "",
  "nominatedPaymentAmountPercentage": "10",
  "nominatedType": "1",
  "paymentExpiryDate": "04/12/2022",
  "paymentRemittanceMethod": "0",
  "paymentStartDate": "04/01/2022",
  "paymentType": "0",
  "routingBankID": "654321"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000139/directDebitControls",
    "invalid-params": [
      "V5BS0010SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*