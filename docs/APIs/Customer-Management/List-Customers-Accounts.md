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
  "customerInformationRes": {
    "businessUnit": 200,
    "customerNumber": "0000020000067163587",
    "givenName": "Andre",
    "externalId": "113902",
    "gender": "0",
    "birthDate": "14/11/1940",
    "nameLine1": "Andre Reichel",
    "addressLine1": "10 4601 Denesik Overpass",
    "addressLine2": "Lake Ofelia,QLD",
    "addressLine3": "Clayfield QLD",
    "addressLine4": "",
    "emailAddress": "Andre.Reichel@company1.com",
    "homePhoneNumber": "++61430010348",
    "workPhoneNumber": "++61430010348",
    "mobileNumber": "++61430010348",
    "numberOfAccounts": 1,
    "isReturnMailEnabled": "N"
  },
  "accountListRes": [
    {
      "accountId": "0001000011000052268",
      "productId": 1,
      "statusOfAccount": "D",
      "memoCreditAmount": "$0.00",
      "memoDebitAmount": "$0.00",
      "mailingIndicator": " ",
      "ddaAccountId": "890005226",
      "isSuppressTokenEnabled": "0",
      "reissueControlMethod": "0",
      "noOfTokenizedCards": 0,
      "blockCode1": "A",
      "blockCode2": "",
      "blockCode1Date": "19/08/2021",
      "blockCode2Date": "00/00/0000"
    }
  ]
}
```

### Error Response Payload

```json
{
  "errorCode": "V5DB4001SF",
  "errorMessage": "AMNA org not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer identification can not be spaces |
| `V5DB4001SF` |AMNA org not found|


