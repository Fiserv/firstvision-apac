# List Customers' Accounts

This API is used to fetch list of accounts and its details associated with a customer Id along with customer demographic information.

## Endpoint

`GET /v1/customers/{customerId}/accountList`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***Customer Identification should be sent as Path Variable.***  

<!--
type: tab
-->

```json
{
  "customerInformation": {
    "businessUnit": 600,
    "customerId": "0006000011000000707",
    "givenName": "Andre",
    "externalId": "113902",
    "gender": 0,
    "birthDate": "14/11/1940",
    "nameLine1": "Andre Reichel",
    "addressLine1": "10 4601 Denesik Overpass",
    "addressLine2": "Lake Ofelia,QLD",
    "addressLine3": "Clayfield QLD",
    "addressLine4": " ",
    "emailAddress": "Andre.Reichel@company1.com",
    "homePhoneNumber": "++61430010348",
    "workPhoneNumber": "++61430010348",
    "mobileNumber": "++61430010348",
    "totalAccountsCount": 1,
    "isReturnMailEnabled": "N"
  },
  "accountList": [
    {
      "accountId": "0001000011000052268",
      "productId": 1,
      "status": "D",
      "memoCreditAmount": "$0.00",
      "memoDebitAmount": "$0.00",
      "mailingIndicator": " ",
      "ddaAccountId": "890005226",
      "isSuppressTokenEnabled": 0,
      "reissueControlMethod": 0,
      "totalTokenizedCardCount": 0,
      "blockCode1": "A",
      "blockCode2": " ",
      "blockCode1Date": "19/08/2021",
      "blockCode2Date": "00/00/0000",
      "externalContractId": "0000000000012672379",
      "addressId": "HOME"
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
    "errorCode": "440401",
    "instance": "/v1/customers/0006000011000000701/accountList",
    "invalid-params": [
      "V5DB4001AS: CUST NBR NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/accountList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer identification can not be spaces |
| `V5DB4001SF` | AMNA org not found |
| `V5DB4001AS` | Cust nbr not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
