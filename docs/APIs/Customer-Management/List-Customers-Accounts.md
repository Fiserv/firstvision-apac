# List Customers' Accounts

The service provides list of accounts associated with the customer. This API also retrive the other information like memo credit/debit balance, block codes and so on.

## Endpoint

`GET /v1/customers/{customerId}/accountList`

## Payload Example

### Request Payload

>Should be empty.  
>
>***Customer Identification should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/accountList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Successful Response Payload

```json
{
  "accountList": [
    {
      "accountId": "0006000012000000121",
      "blockCode1": " ",
      "blockCode1Date": "00/00/0000",
      "blockCode2": " ",
      "blockCode2Date": "00/00/0000",
      "ddaAccountId": "0",
      "isSuppressTokenEnabled": "0",
      "mailingIndicator": " ",
      "memoCreditAmount": "$0.00",
      "memoDebitAmount": "$0.00",
      "noOfTokenizedCards": 0,
      "productId": 1,
      "reissueControlMethod": "0",
      "status": "N",
      "externalContractId": "990012679902",
      "addressId": "HOME9902"
    }
  ],
  "customerInformation": {
    "addressLine1": "HOUSE NO.102",
    "addressLine2": "",
    "addressLine3": "",
    "addressLine4": "",
    "birthDate": "01/02/2010",
    "businessUnit": 600,
    "customerId": "0006000011000000707",
    "emailAddress": "123@FISERV.COM",
    "externalId": "",
    "gender": "1",
    "givenName": "JOHN",
    "homePhoneNumber": "12345",
    "isReturnMailEnabled": "N",
    "mobileNumber": "8877665544",
    "nameLine1": "JOHN DSOUZA",
    "totalAccountsCount": 1,
    "workPhoneNumber": "67894"
  }
}
```

### Error Response Payload

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

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer identification can not be spaces |
| `V5DB4001SF` | AMNA org not found |
| `V5DB4001AS` | Cust nbr not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
