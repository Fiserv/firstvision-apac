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
      "status": "N"
    }
  ],
  "cardtList": [
    {
      "accountId": "0006000012000000121",
      "blockCode": " ",
      "blockCodeDate": "00/00/0000",
      "cardActivatedDate": "00/00/0000",
      "cardHolderType": 1,
      "cardIssueDate": "00/00/0000",
      "cardOpenedDate": "19/08/2021",
      "cardTechnology": "3",
      "chequeAccountId": " ",
      "currentCardAction": "1",
      "currentCardNeedActivation": "Y",
      "digitalID": " ",
      "embosserName2": " ",
      "expirationDate": "18/01/2024",
      "isAtmEnabled": "Y",
      "isCashBackEnabled": "N",
      "isEcomEnabled": 1,
      "isInternationalAtmPosEnabled": "N",
      "isMotoEnabled": "N",
      "isPayWaveEnabled": "N",
      "isPosEnabled": "Y",
      "lastCardAction": "0",
      "lastCardExpirationDate": "00/00/0000",
      "lastCardNeedActivation": "N",
      "lastPlasticIssueDate": 0,
      "lastPlasticSuppressedDate": "0",
      "lastPlasticUsedDate": "0",
      "lastWalletUsedDate": "0",
      "maskedPaymentCardNumber": "000444001XXXXXX8266",
      "mccLimit01": "$999,999,999.99",
      "mccLimit02": "$999,999,999.99",
      "mccLimit03": "$999,999,999.99",
      "mccLimit04": "$999,999,999.99",
      "mccLimit05": "$999,999,999.99",
      "mccLimit06": "$999,999,999.99",
      "mccLimit07": "$999,999,999.99",
      "mccLimit08": "$0.00",
      "mccLimit09": "$0.00",
      "mccLimit10": "$0.00",
      "nameOnCard": "JOHN1",
      "numberOfTokens": 0,
      "paymentInstrumentId": "0004440010880488266",
      "pinOffset": 0,
      "plasticSuppressStatus": "N",
      "productDescription": "VISA CREDIT CONSUMER",
      "savingsAccountId": " ",
      "statusOfCard": "0",
      "warningCode1": "0"
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
    "numberOfAccounts": 1,
    "numberOfCards": 1,
    "workPhoneNumber": "67894"
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*
