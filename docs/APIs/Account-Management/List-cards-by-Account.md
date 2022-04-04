# List cards by Account

The service is used for the purpose of the card look up where the account number is provided and service will send all cards associated with account.

## Endpoint

`POST /v1/accounts/{accountNumber}/listCardsByAccount`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/listCardsByAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Payload | *string* | 19 | Unique Identification number of the Account.|

### Successful Response Payload

```json
{
  "listOfCardsRes": [
    {
      "accountNumber": "0006000022000000076",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 1,
      "cardNumber": "0004440020051355558",
      "nameOnCard": "",
      "status": "1"
    }
  ]
}
```


