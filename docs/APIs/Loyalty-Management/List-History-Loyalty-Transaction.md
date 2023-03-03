# List History Transaction

This API is used to fetch History transactions. This API displays all point transactions that have posted, appeared on a statement, and settled with the store.

## Endpoint

`GET /v1/loyalty/{accountId}/listHistoryTransaction`

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
      "effectiveDate": "15/08/2025",
      "loyaltyPoints": "0",
      "postingDate": "15/08/2025",
      "rate": "000000000",
      "recordNumber": 7,
      "storeName": "CREDIT",
      "transactionAmount": "$196.44",
      "transactionCode": "002",
      "transactionDescription": "CREDIT"
    },
    {
      "effectiveDate": "15/08/2025",
      "loyaltyPoints": "196",
      "postingDate": "15/08/2025",
      "rate": "010000000",
      "recordNumber": 9,
      "storeName": "CREDIT",
      "transactionAmount": "$196.44",
      "transactionCode": "070",
      "transactionDescription": "CREDIT"
    },
    {
      "effectiveDate": "15/03/2022",
      "loyaltyPoints": "27300",
      "postingDate": "09/04/2022",
      "rate": "000000000",
      "recordNumber": 1,
      "storeName": "PRIMECREDIT LIMITED",
      "transactionAmount": "$0.00",
      "transactionCode": "051",
      "transactionDescription": "AUTO DISBURSEME"
    },
    {
      "effectiveDate": "08/02/2022",
      "loyaltyPoints": "3000",
      "postingDate": "08/02/2022",
      "rate": "000000000",
      "recordNumber": 0,
      "storeName": "PRIMECREDIT LIMITED",
      "transactionAmount": "$0.00",
      "transactionCode": "051",
      "transactionDescription": "REDEEMED POINTS"
    },
    {
      "effectiveDate": "17/02/2017",
      "loyaltyPoints": "800",
      "postingDate": "18/02/2017",
      "rate": "000000000",
      "recordNumber": 1,
      "storeName": "PRIMECREDIT LIMITED",
      "transactionAmount": "$0.00",
      "transactionCode": "051",
      "transactionDescription": "AUTO DISBURSEME"
    },
    {
      "effectiveDate": "23/01/2017",
      "loyaltyPoints": "0",
      "postingDate": "23/01/2017",
      "rate": "000000000",
      "recordNumber": 1,
      "storeName": "INT'L RETAIL SALE",
      "transactionAmount": "$139.90",
      "transactionCode": "001",
      "transactionDescription": "INT'L RETAIL SA"
    },
    {
      "effectiveDate": "23/01/2017",
      "loyaltyPoints": "140",
      "postingDate": "23/01/2017",
      "rate": "010000000",
      "recordNumber": 3,
      "storeName": "INT'L RETAIL SALE",
      "transactionAmount": "$139.90",
      "transactionCode": "050",
      "transactionDescription": "INT'L RETAIL SA"
    },
    {
      "effectiveDate": "23/01/2017",
      "loyaltyPoints": "0",
      "postingDate": "23/01/2017",
      "rate": "000000000",
      "recordNumber": 4,
      "storeName": "RETAIL SALE",
      "transactionAmount": "$660.28",
      "transactionCode": "001",
      "transactionDescription": "RETAIL SALE"
    },
    {
      "effectiveDate": "23/01/2017",
      "loyaltyPoints": "660",
      "postingDate": "23/01/2017",
      "rate": "010000000",
      "recordNumber": 6,
      "storeName": "RETAIL SALE",
      "transactionAmount": "$660.28",
      "transactionCode": "050",
      "transactionDescription": "RETAIL SALE"
    },
    {
      "effectiveDate": "20/12/2016",
      "loyaltyPoints": "34833",
      "postingDate": "29/12/2016",
      "rate": "000000000",
      "recordNumber": 25,
      "storeName": "RETAIL SALE 071ST      US            US",
      "transactionAmount": "$6,966.64",
      "transactionCode": "052",
      "transactionDescription": "RETAIL SALE 071"
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
    "instance": "/v1/loyalty//listHistoryTransaction",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loyalty/{accountId}/listHistoryTransaction).

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
