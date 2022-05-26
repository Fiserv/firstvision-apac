# List Cards by Account

The service is used for the purpose of the card look up where the account number is provided and service will send all cards associated with account.

## Endpoint

`GET /v1/accounts/{accountId}/listCardsByAccount`

## Payload Example

### Request Payload

>Should be empty.
>
>***Account id should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/listCardsByAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Successful Response Payload

```json

{
  "listOfCardsRes": [
    {
      "accountId": "0006000022000000076",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 1,
      "nameOnCard": "",
      "paymentInstrumentId": "0004440020051355558",
      "status": "1"
    }
  ]
}

```


