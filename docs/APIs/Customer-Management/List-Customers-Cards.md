# List Customers' Cards

This API is used to fetch the list of cards and its details associated with a customer Id along with customer demographic information.

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
  "cardList": [
    {
      "accountId": "0006000012000000121",
      "addressId": " ",
      "blockCode": " ",
      "blockCodeDate": "00/00/0000",
      "cardActivatedDate": "00/00/0000",
      "cardHolderType": 1,
      "cardIssueDate": "00/00/0000",
      "cardOpenedDate": "19/08/2021",
      "cardTechnology": 3,
      "chequeAccountId": " ",
      "currentCardAction": 1,
      "currentCardNeedActivation": "Y",
      "dateLastPlasticUsed": "0",
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
      "lastCardAction": 0,
      "lastCardExpirationDate": "00/00/0000",
      "lastCardNeedActivation": "N",
      "lastPlasticIssueDate": 0,
      "lastPlasticSuppressedDate": "0",
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
      "paymentInstrumentId": "0004440010880488266",
      "physicalVirtualIndicator": " ",
      "plasticId": " ",
      "plasticSuppressStatus": "N",
      "productDescription": "VISA CREDIT CONSUMER",
      "savingsAccountId": " ",
      "status": "0",
      "tokenCount": 0,
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
    "gender": 1,
    "givenName": "JOHN",
    "homePhoneNumber": "12345",
    "isReturnMailEnabled": "N",
    "mobileNumber": "8877665544",
    "nameLine1": "JOHN DSOUZA",
    "totalCardsCount": 1,
    "workPhoneNumber": "67894"
  }
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
