# List Visa Token

This API is used to fetch token details like VTS token number, card wallet account id and token requestor/reference id associated with given payment instrument Id.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/listVisaToken`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Payment Instrument Identification should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "tokenList": [
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "586b384a-3b46-410b-9773-8c9720d5",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400001008622786"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "a3763961-2bcc-4b02-b9c3-bb4decd6",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400001018459526"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "071d1012-ff96-4aa8-b799-06effa1a",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400001030832858"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "b7375489-7518-4c36-bc8c-11946f89",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400001032292283"    },
    {
      "tokenRequestorId": "06110030273",
      "tokenReferenceId": "cc15268336bf469abb98431830075259",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400001046883945"    },
    {
      "tokenRequestorId": "06100000005",
      "tokenReferenceId": "ab8fd132ae5f42928d65f3cc5ab08ccb",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400005031196858"    },
    {
      "tokenRequestorId": "06100000005",
      "tokenReferenceId": "f16ae3173df94aa08c6fea051304c4e2",
      "cardWalletAccountId": " ",
      "status": "0",
      "vtsTokenNumber": "5077400005048482515"    }
  ]
}

```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "240010",
    "instance": "/v1/cards/0009545880002462305/listVisaToken",
    "invalid-params": [
      "businessUnit: The maximum value for this field is 999"
    ],
    "source": "APT",
    "status": 400,
    "title": "Constraint(s) Violated"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/listVisaToken).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

*please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
