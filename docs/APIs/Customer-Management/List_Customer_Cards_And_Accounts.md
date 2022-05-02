# List Customers' Cards And Accounts

This service retrieves the account and card details associated with a Customer number along with demographic details.

## Endpoint

`GET /v1/customers/{customerNumber}/listCustomersCardsAndAccounts`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Customer Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/listCustomersCardsAndAccounts).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer.|


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
  "cardtListRes": [
    {
      "accountNumber": "0002000010000400435",
      "atmFlag": "Y",
      "blockCode": " ",
      "blockCodeDate": "00/00/0000",
      "cardActivatedDate": "00/00/0000",
      "cardExpiryDate": "06/04/2024",
      "cardHolderType": 1,
      "cardIssuedDate": "09/04/2021",
      "cardNumber": "0009543491000009551",
      "cardOpenedDate": "07/04/2021",
      "cardTechnology": "3",
      "cashBackTranFlag": "Y",
      "chequeAccountNumber": " ",
      "currentCardAction": "0",
      "currentCardNeedActivation": "Y",
      "dateLastPlasticSuppressed": "0",
      "dateLastPlasticUsed": "0",
      "dateLastWalletUsed": "0",
      "digitalID": " ",
      "ecomActFlag": 1,
      "embosserName2": " ",
      "intAtmPosFlag": "Y",
      "lastCardAction": "1",
      "lastCardExpiryDate": "00/00/0000",
      "lastCardNeedActivation": "Y",
      "maskCardNumber": "000954349XXXXXX9551",
      "mccLimit1": "$999,999,999.99",
      "mccLimit10": "$0.00",
      "mccLimit2": "$999,999,999.99",
      "mccLimit3": "$999,999,999.99",
      "mccLimit4": "$999,999,999.99",
      "mccLimit5": "$999,999,999.99",
      "mccLimit6": "$999,999,999.99",
      "mccLimit7": "$999,999,999.99",
      "mccLimit8": "$0.00",
      "mccLimit9": "$0.00",
      "motoFlag": "Y",
      "nameOnCard": "Andre Reichel",
      "numberOfCards": 0,
      "payWaveFlag": "Y",
      "pinOffset": 0,
      "plasticSuppressStatus": "N",
      "posFlag": "Y",
      "productDescription": "VISA DEBIT PERSONAL",
      "savingsAccountNbr": "1240310048409873",
      "statusOfCard": "0",
      "timeLastPlasticIssue": 210438,
      "warningCode": "0"
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
    "numberOfCards": 1,
    "userDefinedField4": "N",
    "workPhoneNumber": "+61463514716"
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5NA0004SF",
  "errorMessage": "Customer Number Can Not Be Spaces"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer Number Can Not Be Spaces |
| `V5DB4001AS` | Cust Nbr Not Found |
