# List Customers' Cards

This service retrieves the card details associated with a Customer id along with customer demographic information.

## Endpoint

`GET /v1/customers/{customerId}/cardList`

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
    "totalCardsCount": 1,
    "isReturnMailEnabled": "N"
  },
  "cardList": [
    {
      "lastWalletUsedDate": "0",
      "lastPlasticSuppressedDate": "0",
      "cardIssueDate": "28/09/2020",
      "lastCardExpirationDate": "00/00/0000",
      "lastCardNeedActivation": "Y",
      "embosserName2": " ",
      "dateLastPlasticUsed": "10/02/2021",
      "blockCodeDate": "00/00/0000",
      "chequeAccountId": " ",
      "savingsAccountId": " ",
      "currentCardAction": "0",
      "lastCardAction": "1",
      "expirationDate": "16/09/2023",
      "cardActivatedDate": "00/00/0000",
      "mccLimit04": "$0.00",
      "mccLimit05": "$0.00",
      "mccLimit06": "$0.00",
      "mccLimit07": "$0.00",
      "mccLimit08": "$0.00",
      "mccLimit09": "$0.00",
      "mccLimit10": "$0.00",
      "mccLimit02": "$0.00",
      "mccLimit03": "$0.00",
      "lastPlasticIssueDate": 131201,
      "mccLimit01": "$0.01",
      "nameOnCard": "U T UATMLNCUST448",
      "paymentInstrumentId": "0009846801010009405",
      "tokenCount": 0,
      "digitalID": " ",
      "cardOpenedDate": "17/09/2020",
      "accountId": "0001000011000052268",
      "maskedPaymentCardNumber": "000984680XXXXXX9405",
      "productDescription": "VISA PLATINUM DEBIT",
      "isPosEnabled": "Y",
      "isEcomEnabled": "1",
      "isAtmEnabled": "Y",
      "isCashBackEnabled": "Y",
      "isPayWaveEnabled": "Y",
      "isInternationalAtmPosEnabled": "Y",
      "isMotoEnabled": "N",
      "cardHolderType": "1",
      "status": "0",
      "blockCode": " ",
      "currentCardNeedActivation": "Y",
      "cardTechnology": "3",
      "warningCode1": "0",
      "plasticSuppressStatus": "N",
      "physicalVirtualIndicator": "V",
      "addressId": "HOME",
      "plasticId": " "
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
    "instance": "/v1/customers/0006000011000000701/cardList",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/customers/{customerId}/cardList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5NA0004SF` | Customer number can not be spaces |
| `V5DB4001SF` | AMNA org not found |
| `V5DB4001AS` | Cust nbr not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*