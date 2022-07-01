# List Visa Token

This service is used to inquire token detail like VTS token number, card wallet account id and token requestor/reference id associated with given payment instrument identification.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/listVisaToken`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Payment Instrument Identification should be sent as path variable..***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/listVisaToken).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Successful Response Payload

```json
{
  "tokenList": [
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "586b384a-3b46-410b-9773-8c9720d5",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400001008622786"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "a3763961-2bcc-4b02-b9c3-bb4decd6",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400001018459526"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "071d1012-ff96-4aa8-b799-06effa1a",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400001030832858"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "b7375489-7518-4c36-bc8c-11946f89",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400001032292283"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "cc15268336bf469abb98431830075259",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400001046883945"    },
    {
      "tokenRequestorId": "06100000005",
      "tokenReferenceId": "ab8fd132ae5f42928d65f3cc5ab08ccb",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400005031196858"    },
    {
      "tokenRequestorId": "06100000005",
      "tokenReferenceId": "f16ae3173df94aa08c6fea051304c4e2",
      "cardhWalletAcctId": " ",
      "vtsTokenNumber": "5077400005048482515"    }
  ]
}

```

### Error Response Payload

*Please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*

