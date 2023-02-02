# List Cards by Account

The service is used for the purpose of the card look up where the account number is provided and service will send all cards associated with account.

## Endpoint

`GET /v1/accounts/{accountId}/listCardsByAccount`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "listOfCards": [
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

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "240010",
    "instance": "/v1/accounts/0006000011000000161/listCardsByAccount",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/listCardsByAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|


### Error Codes

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*


