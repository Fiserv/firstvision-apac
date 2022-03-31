# List Customers' Accounts

The service provides list of accounts associated with the customer. This API also retrive the other information like memo credit/debit balance, block codes and so on.

## Endpoint

`GET /v1/customers/{customerNumber}/accountList`

## Payload Example

### Request Payload

>Shoud be empty.  
***Customer Number should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/accountList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer. |

### Successful Response Payload

```json

{
  "accountList": [
    {
      "accountNumber": "0001000011000052268",
      "amountMemoCredit": "$0.00",
      "amountMemoDebit": "$0.00",
      "blockCode1": " ",
      "blockCode1Date": "00/00/0000",
      "blockCode2": " ",
      "blockCode2Date": "00/00/0000",
      "businessUnit": "100",
      "ddaAccountNumber": "890005226",
      "internalStatus": "D",
      "mailingIndicator": " ",
      "nbrOfTokenizedCards": 0,
      "product": "1",
      "reissContolMethod": 0,
      "suppressToken": "0"
    }
  ],
  "addressLine1": "62 CHARTERIS DR",
  "addressLine2": "",
  "addressLine3": "",
  "addressLine4": "",
  "billingLvl": "0",
  "businessUnit": "0",
  "creditLimit": "$0.00",
  "customerName": "UATMFNCU448",
  "customerNumber": "0001000000000113902",
  "dateOfBirth": "14/11/1940",
  "emailAddress": "UATMFNCU448@GMAIL.COM",
  "gender": "0",
  "homeDistricName": "",
  "homePhoneNumber": "++61430010348",
  "mobileNumber": "++61430010348",
  "nameLine1": "UATMFNCU448 TWOPPPUATMLNCUST448",
  "numberOfAccounts": "1",
  "numberOfCards": "1",
  "relName": "",
  "relationshipNbr": "",
  "ssnId": "113902",
  "status": "",
  "totalAvailable": "$0.00",
  "userDefinedField4": "Y",
  "workPhoneNumber": "++61430010348"
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
