# List External Customers' Cards And Accounts

This API is used to fetch the list of accounts, list of cards and it's details associated with an external contract Id.

## Endpoint

`GET /v1/customers/{externalContractId}/listExternalCustomersCardsAndAccounts`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The External Customer Identifiaction should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "externalContractId": "0000000000012672379",
  "totalAccountsCount": 2,
  "totalCardsCount": 2,
  "businessUnit": 600,
  "accountList": [
    {
      "accountId": "0006000012000000256",
      "productId": 1,
      "status": "A",
      "transferFromOrTransferToAccountId": "0006000012000000123",
      "addressId": "RESIDENTIAL",
      "blockCode1": "A",
      "blockCode2": " ",
      "shortName": "Dhruv",
      "residenceId": "SX1",
      "customerId": "0000020000065439605"
    }
  ],
  "cardList": [
    {
      "paymentInstrumentId": "0009544410000000047",
      "blockCode": " ",
      "embossedName": "DAVID TEST 2",
      "addressId": "RESIDENTIAL",
      "plasticId": " ",
      "accountId": "0006000012000000256",
      "expiryDate": "16/08/2024",
      "transferFromPaymentInstrumentId": "0009543161000134358",
      "transferToPaymentInstrumentId": "0009543160010000062",
      "maskedPaymentCardNumber": "000431683XXXXXX0959"
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
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/customers/09993499789916/listExternalCustomersCardsAndAccounts",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5D14001SF: AMCIDX - REC NOT FOUND"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{externalContractId}/listExternalCustomersCardsAndAccounts).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `externalContractId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer from external system.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5D14001SA` | Invalid CCID |
| `V5D14001SF` | AMCIDX - Rec not found |
| `V5D14001SB` | AMBS - Account not found |
| `V5D14001SC` | AMBS - Account is in add pending |
| `V5D14001SD` | AMBS - Rec purged |
| `V5D14001SE` | AMAX - Record not found |
| `V5D14001SH` | AMED - Rec not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
