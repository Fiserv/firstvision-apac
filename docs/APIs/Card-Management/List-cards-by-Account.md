# List cards by Account

The service is used for the purpose of the card look up where the account number is provided and service will send all cards associated with account.

## Endpoint

`GET /v1/accounts/{accountNumber}/listCardsByAccount`

## Payload Example

### Request Payload

> Should be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/listCardsByAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the account.|

### Successful Response Payload

```json
{
  "listOfCards": [
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010015644528",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010020927363",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010044487782",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010058164574",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010084810463",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 1,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010092387371",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010262797243",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010369465561",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010388834920",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010415574424",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010425015947",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010462782698",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010501612690",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010554156348",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010572183043",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010613722064",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010641905491",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010698097747",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010698241410",
      "status": "1"
    },
    {
      "accountNumber": "0004440010000000017",
      "blockCode": "",
      "businessUnit": 600,
      "cardHolderType": 0,
      "embeddedCardBusinessUnit": "600",
      "embeddedCardNumber": "0004440010731293865",
      "status": "1"
    }
  ]
}
```


