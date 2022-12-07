# List External Customers' Cards And Accounts

This service retrieves the account and cards details associated with an external customer ID.

## Endpoint

`GET /v1/customers/{externalContractId}/listExternalCustomersCardsAndAccounts`

## Payload Example

### Request Payload

>Should be empty.
>
>***The External Customer Identifiaction should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{externalContractId}/listExternalCustomersCardsAndAccounts).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `externalContractId` | Path Variable | *string* | 14 | Unique identification number assigned to a customer from external system.|


### Successful Response Payload

```json
{
    "accountList": {
        "blockCode2": "",
        "shortName": "SRAVANTHI",
        "residenceId": "B01",
        "totalCardsCount": 3,
        "businessUnit": 700,
        "productId": 1,
        "accountId": "0007000011925283501",
        "status": "N",
        "memoDebitAmount": "0.00",
        "blockCode1": "",
        "addressId": "12"
    },
    "cardList": [
        {
            "paymentInstrumentId": "0009543161000021084",
            "blockCode1": " ",
            "embossedName": "SRAVANTHI9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/06/2025"
        },
        {
            "paymentInstrumentId": "0009543161000021126",
            "blockCode1": " ",
            "embossedName": "SRAVANTHI9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/04/2025"
        },
        {
            "paymentInstrumentId": "0009543161000023601",
            "blockCode1": " ",
            "embossedName": "chsrabc9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/10/2025"
        }
    ],
    "externalContractId": "99993499789916"
}
```

### Error Response Payload

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
