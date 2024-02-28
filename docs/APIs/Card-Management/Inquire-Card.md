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
  "accountId": "0006000022000000050",
  "addressFields": {
    "addressId": "",
    "addressLine1": "FISERV",
    "addressLine2": "NAB",
    "city": "CHENNAI",
    "postalCode": "",
    "stateProvince": ""
  },
  "authorizationCriteriaTableId": "800",
  "blockCodeDetails": {
    "blockCode": "X",
    "blockDate": "19/08/2021",
    "blockSecurityId": "NAB"
  },
  "businessUnit": 600,
  "cardAction": 1,
  "cardDelayDaysCount": 0,
  "cardReissueDeliveryLocation": 0,
  "cardReissueDeliveryOption": "5",
  "cardRequestedCount": 1,
  "cardReturnedCount": 0,
  "cardType": 0,
  "cardTypeRequested": 0,
  "cardholderType": 1,
  "currentCardNeedActivation": "N",
  "customerId": "",
  "customersGender": 0,
  "dateFields": {
    "cardActivatedDate": "00/00/0000",
    "cardIssueDate": "00/00/0000",
    "currentCardValidDate": "00/00/0000",
    "expiryDate": "17/08/2024",
    "firstCardVerifyDate": "00/00/0000",
    "lastCardExpiryDate": "00/00/0000",
    "mailerDate": "00/00/0000",
    "nextCardExpiryDate": "00/00/0000",
    "statusChangeDate": "00/00/0000",
    "transferEffectiveDate": "00/00/0000"
  },
  "digitalId": "",
  "emblemId": 0,
  "externalContractId": "",
  "firstIssueBranch": 0,
  "fraudTransferPaymentInstrumentId": "",
  "isDynamicCVV2Enabled": "",
  "isPinSuppressionEnabled": 0,
  "isSecureCodeEnabled": 0,
  "lastCardActivation": "N",
  "maskedPaymentCardNumber": "",
  "mobileDeviceID": "",
  "mobileProvisionStatus": 0,
  "nameFields": {
    "cardholderName1": "",
    "cardholderName2": "",
    "embossedName1": "R0203 CARDHOLDER#3",
    "embossedName2": "FISERV DEMO FACILITY",
    "name1TypeIndicator": 0,
    "name2TypeIndicator": 0
  },
  "numberOfCardsOutstanding": 0,
  "paymentInstrumentId": "0009544410000000047",
  "physicalVirtualIndicator": "",
  "pinDelayDaysCount": 0,
  "pinOverride": "1",
  "plasticId": "VISA001",
  "posServiceCode": "",
  "productId": 2,
  "reasonCode": "",
  "reissueAttemptCount": 0,
  "status": "0",
  "transferFromPaymentInstrumentId": "",
  "transferToPaymentInstrumentId": "",
  "userDefinedFields": {
    "field1": "",
    "field2": "",
    "field3": "",
    "field4": 0,
    "field5": ""
  },
  "visaMiniCardVersion": 0,
  "visaPlusIndicator": 0,
  "warningCodeDetails": {
    "warningCode1": "1",
    "warningCode1SetDate": "18/08/2021",
    "warningCode7": "0"
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
