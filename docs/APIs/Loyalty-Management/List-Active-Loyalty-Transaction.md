# List Active Transaction

This API is used to fetch Active transactions. This API displays the point transactions that have been calculated and posted but either a statement has not been produced for the account and/or the transactions have not been settled with the store.

## Endpoint

`GET /v1/loyalty/{accountId}/listActiveTransaction`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable and schemeId, businessUnit should be sent as query parameters.***

<!--
type: tab
-->

```json
{
  "accountId": "0000000000000000001",
  "businessUnit": 600,
  "schemeId": "10101",
  "schemeName": "",
  "transactionList": [
    {
      "effectiveDate": "17/01/2021",
      "loyaltyPoints": "100000",
      "postingDate": "17/01/2021",
      "rate": "000000000",
      "recordNumber": 0,
      "storeName": "TESTING VMA LMS",
      "transactionAmount": "$0.00",
      "transactionCode": "050",
      "transactionDescription": "EARNED POINTS C"
    },
    {
      "effectiveDate": "17/01/2021",
      "loyaltyPoints": "100000",
      "postingDate": "17/01/2021",
      "rate": "000000000",
      "recordNumber": 152203,
      "storeName": " ",
      "transactionAmount": "$0.00",
      "transactionCode": "056",
      "transactionDescription": "BOUGHT POINTS C"
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
    "errorCode": "240401",
    "instance": "/v1/loyalty//listActiveTransaction",
    "invalid-params": [
      "No API exist for this instance"
    ],
    "source": "APT",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loyalty/{accountId}/listActiveTransaction).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number that identifies the points account. |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `schemeId` | Query Parameter | *number* | 5 | Unique identification number of the points scheme associated with the organization. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VKQT4003SA` | Invalid account - must be numeric |
| `VKQT4001SA` | Record is in an add pending state |
| `VKQT4001SB` | Record is not active |
| `VKQT4001SC` | Organization not on file |
| `VKQT4003EA` | Invalid account |
| `VKQT4004SA` | Invalid scheme Id |
| `VKQT4005EB` | Invalid from effective date |
| `VKQT4005SA` | Invalid from effective date |
| `VKQT4006EB` | Invalid to effective date |
| `VKQT4006SA` | Invalid to effective date |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
