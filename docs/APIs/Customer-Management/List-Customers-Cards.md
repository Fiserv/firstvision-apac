# List Customers' Cards

The service provides list of cards associated with the customer. FirstVision allows to retrive card details either using account or customer number.

## Endpoint

`GET /v1/customers/{customerNumber}/cardList/`

## Payload Example

### Request Payload

>Shoud be empty.  
***Customer Number should be sent as Path Variable.***  

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerNumber}/cardList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerNumber` | Path Variable | *string* | 19 | An identifier of the customer. |

### Successful Response Payload

```json
{
  "addressLine1": "62 CHARTERIS DR",
  "addressLine2": "",
  "addressLine3": "",
  "addressLine4": "",
  "billingLvl": "0",
  "businessUnit": "0",
  "cardList": [
    {
      "atmFlag": "Y",
      "blockCode": " ",
      "blockDate": "00/00/0000",
      "businessUnit": 100,
      "cardActivatedDate": "00/00/0000",
      "cardExpirationDate": "16/09/2023",
      "cardIssueDate": "28/09/2020",
      "cardNumber": "0009846801010009405",
      "cardSequence": 1,
      "cardTechnology": "3",
      "cardholderType": 1,
      "cashBackTranFlag": "Y",
      "chequeAccountNbr": " ",
      "currCardAction": "0",
      "currentCardNeedActivation": "Y",
      "dateLastPlasticSupresed": "0",
      "dateLastPlasticUsed": "0",
      "dateLastWalletUsed": "0",
      "dateOpened": "17/09/2020",
      "digitalId": " ",
      "e-comActFlag": "1",
      "embosserRecordStatus": "0",
      "embrName2": " ",
      "intAtmPosFlag": "Y",
      "lastCardAction": "1",
      "lastCardExpirationDate": "00/00/0000",
      "lastCardNeedActivation": "Y",
      "maskCardNumber": "000984680XXXXXX9405",
      "mccLimit-1": "$0.01",
      "mccLimit-10": "$0.00",
      "mccLimit-2": "$0.00",
      "mccLimit-3": "$0.00",
      "mccLimit-4": "$0.00",
      "mccLimit-5": "$0.00",
      "mccLimit-6": "$0.00",
      "mccLimit-7": "$0.00",
      "mccLimit-8": "$0.00",
      "mccLimit-9": "$0.00",
      "motoFlag": " ",
      "nameOnCard": "U T UATMLNCUST448",
      "numberOfCards": "0",
      "payWaveFlag": "Y",
      "pinOffset": "329861",
      "plasticSuppressStatus": "N",
      "posFlag": "Y",
      "postToAccount": "0001000011000052268",
      "product": 1,
      "productDescription": "VISA PLATINUM DEBIT",
      "savingsAccountNbr": " ",
      "timeLastPlasticIssue": 13815,
      "warningCode": "0"
    }
  ],
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
  "workPhoneNumber": "+61430010348"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5DB4001AS",
  "errorMessage": "Customer Nbr not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5DB4001AS` |Customer Nbr not found|
