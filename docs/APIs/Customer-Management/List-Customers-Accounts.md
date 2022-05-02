# List Customers' Accounts

The service provides list of accounts associated with the customer. This API also retrive the other information like memo credit/debit balance, block codes and so on.

## Endpoint

`GET /v1/customers/{customerNumber}/accountList`

## Payload Example

### Request Payload

>Should be empty.  
>
>***Customer Number should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/accountList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer. |

### Successful Response Payload

```json
{
  "accountListRes": [
    {
      "accountNumber": "0002000010000400435",
      "blockCode1": " ",
      "blockCode1Date": "00/00/0000",
      "blockCode2": " ",
      "blockCode2Date": "00/00/0000",
      "ddaAccountNumber": "1240310048409873",
      "mailingIndicator": " ",
      "memoCreditAmount": "$0.00",
      "memoDebitAmount": "$0.00",
      "noOfTokenizedCards": 0,
      "product": 1,
      "reissueControlMethod": "0",
      "statusOfAccount": "D",
      "suppressToken": "0"
    }
  ],
  "customerInformationRes": {
    "addressLine1": "10 4601 Denesik Overpass",
    "addressLine2": "Lake Ofelia,QLD",
    "addressLine3": "Clayfield QLD",
    "addressLine4": "",
    "businessUnit": 200,
    "customerName": "Andre Reichel",
    "customerNumber": "0000020000067163587",
    "dateOfBirth": "21/10/1971",
    "emailAddress": "Andre.Reichel@company1.com",
    "firstName": "Andre",
    "gender": "2",
    "homePhoneNumber": "+61463514716",
    "identificationNumber": "67163587",
    "mobileNumber": "+61463514716",
    "numberOfAccounts": 1,
    "userDefinedField4": "N",
    "workPhoneNumber": "+61463514716"
  }
}

```

### Error Response Payload

```json
{
  "errorCode": "V5DB4001AS",
  "errorMessage": "Customer nbr not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5DB4001AS` |Customer nbr not found|
