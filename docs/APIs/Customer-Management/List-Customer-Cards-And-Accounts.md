# List Customers' Cards And Accounts

This service retrieves the account and card details associated with a Customer number along with demographic details.

## Endpoint

`GET /v1/customers/{customerId}/listCustomersCardsAndAccounts`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Customer Identifiaction should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/listCustomersCardsAndAccounts).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer.|


### Successful Response Payload

```json
{
  "accountListRes": [
    {
      "accountId": "0002000010000400435",
      "blockCode1": " ",
      "blockCode1Date": "00/00/0000",
      "blockCode2": " ",
      "blockCode2Date": "00/00/0000",
      "ddaAccountId": "1240310048409873",
      "isSuppressTokenEnabled": "0",
      "mailingIndicator": " ",
      "memoCreditAmount": "$0.00",
      "memoDebitAmount": "$0.00",
      "noOfTokenizedCards": 0,
      "productId": 1,
      "reissueControlMethod": "0",
      "statusOfAccount": "D"
    }
  ],
  "cardtListRes": [
    {
      "accountId": "0002000010000400435",
      "blockCode": " ",
      "blockCodeDate": "00/00/0000",
      "cardActivatedDate": "00/00/0000",
      "cardHolderType": 1,
      "cardIssueDate": "09/04/2021",
      "cardOpenedDate": "07/04/2021",
      "cardTechnology": "3",
      "chequeAccountId": " ",
      "currentCardAction": "0",
      "currentCardNeedActivation": "Y",
      "lastPlasticUsedDate": "0",
      "digitalID": " ",
      "embosserName2": " ",
      "expirationDate": "06/04/2024",
      "isAtmEnabled": "Y",
      "isCashBackEnabled": "Y",
      "isEcomEnabled": 1,
      "isInternationalAtmPosEnabled": "Y",
      "isMotoEnabled": "Y",
      "isPayWaveEnabled": "Y",
      "isPosEnabled": "Y",
      "lastCardAction": "1",
      "lastCardExpirationDate": "00/00/0000",
      "lastCardNeedActivation": "Y",
      "lastPlasticIssueDate": 210438,
      "lastPlasticSuppressedDate": "0",
      "lastWalletUsedDate": "0",
      "maskedPaymentInstrumentId": "000954349XXXXXX9551",
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
      "nameOnCard": "Andre Reichel",
      "numberOfTokens": 0,
      "paymentInstrumentId": "0009543491000009551",
      "pinOffset": 0,
      "plasticSuppressStatus": "N",
      "productDescription": "VISA DEBIT PERSONAL",
      "savingsAccountId": "1240310048409873",
      "statusOfCard": "0",
      "warningCode1": "0"
    }
  ],
  "customerInformationRes": {
    "addressLine1": "10 4601 Denesik Overpass",
    "addressLine2": "Lake Ofelia,QLD",
    "addressLine3": "Clayfield QLD",
    "addressLine4": "",
    "birthDate": "21/10/1971",
    "businessUnit": 200,
    "customerId": "0000020000067163587",
    "emailAddress": "Andre.Reichel@company1.com",
    "externalId": "67163587",
    "gender": "2",
    "givenName": "Andre",
    "homePhoneNumber": "+61463514716",
    "isReturnMailEnabled": "N",
    "mobileNumber": "+61463514716",
    "nameLine1": "Andre Reichel",
    "numberOfAccounts": 1,
    "numberOfCards": 1,
    "workPhoneNumber": "+61463514716"
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5NA0004SF",
  "errorMessage": "Customer Number can not be spaces"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer Number can not be spaces |
| `V5DB4001SF` | AMNA org not found |
