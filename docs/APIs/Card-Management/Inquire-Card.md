# Inquire Card

This API is used to fetch detailed information for a given payment instrument Id. This API response provides information about card demographic and processing parameters.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***The Payment Instrument Identification should be sent as path variable.***

<!--
type: tab
-->

```json

{
  "businessUnit": 600,
  "paymentInstrumentId": "0009544410000000047",
  "accountId": "0006000022000000076",
  "productId": 1,
  "status": "0",
  "numberOfCardsOutstanding": 1,
  "cardReturnedCount": 0,
  "cardAction": "1",
  "cardRequestedCount": 1,
  "cardType": 0,
  "cardTypeRequested": 0,
  "isSecureCodeEnabled": "0",
  "visaPlusIndicator": "0",
  "customerId": " ",
  "posServiceCode": " ",
  "cardholderType": "0",
  "pinDelayDaysCount": 0,
  "visaMiniCardVersion": "0",
  "isPinSuppressionEnabled": "0",
  "reissueAttemptCount": 0,
  "currentCardNeedActivation": "N",
  "lastCardActivation": "N",
  "fraudCardTransferCount": " ",
  "cardReissueDeliveryLocation": 0,
  "cardReissueDeliveryOption": "0",
  "firstIssueBranch": 0,
  "authorizationCriteriaTableId": " ",
  "emblemId": 0,
  "cardDelayDaysCount": 0,
  "customersGender": "0",
  "reasonCode": "",
  "pinOverride": "0",
  "mobileDeviceID": "",
  "mobileProvisionStatus": "0",
  "digitalId": "0",
  "addressFields": {
    "addressLine1": " ",
    "addressLine2": " ",
    "city": " ",
    "stateProvince": " ",
    "postalCode": " ",
    "addressId": "HOME"
  },
  "userDefinedFields": {
    "field1": " ",
    "field2": " ",
    "field3": " ",
    "field4": 0,
    "field5": " "
  },
  "nameFields": {
    "cardholderName1": " ",
    "cardholderName2": " ",
    "embossedName1": "DAVID TEST 2",
    "embossedName2": " ",
    "name1TypeIndicator": "0",
    "name2TypeIndicator": "0"
  },
  "dateFields": {
    "expiryDate": "16/08/2024",
    "statusChangeDate": "01/02/2020",
    "transferEffectiveDate": "01/02/2020",
    "lastCardExpiryDate": "01/02/2020",
    "cardActivatedDate": "19/08/2021",
    "cardIssueDate": "01/02/2020",
    "currentCardValidDate": "01/02/2022",
    "mailerDate": "01/02/2020",
    "nextCardExpiryDate": "01/02/2020",
    "firstCardVerifyDate": "01/02/2020"
  },
  "warningCodeDetails": {
    "warningCode7": "0",
    "warningCode1": "0",
    "warningCode1SetDate": "00/00/0000"
  },
  "blockCodeDetails": {
    "blockSecurityId": " ",
    "blockCode": " ",
    "blockDate": "25/01/202"
  },
  "externalContractId": "000012672379",
  "physicalVirtualIndicator": "V",
  "isDynamicCVV2Enabled": "0",
  "plasticId": " ",
  "maskedPaymentCardNumber": "000484680XXXXXX9405"
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
    "instance": "/v1/cards/0009544410000000041/details",
    "invalid-params": [
      "V5ED0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/details).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
