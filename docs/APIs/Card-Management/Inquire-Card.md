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
    "addressFields": {
        "addressLine1": "DUMMY",
        "addressLine2": "",
        "city": "",
        "stateProvince": "",
        "postalCode": "",
        "addressId": "awedrffg"
    },
    "userDefinedFields": {
        "field1": "",
        "field2": "",
        "field3": "",
        "field4": 0,
        "field5": ""
    },
    "nameFields": {
        "cardholderName1": "",
        "cardholderName2": "",
        "embossedName1": "EMB1",
        "embossedName2": "EMB2",
        "name1TypeIndicator": "0",
        "name2TypeIndicator": "0"
    },
    "dateFields": {
        "expiryDate": "12/07/2026",
        "transferEffectiveDate": "00/00/0000",
        "lastCardExpiryDate": "12/07/2026",
        "cardIssueDate": "17/04/2023",
        "currentCardValidDate": "01/04/2023",
        "mailerDate": "00/00/0000",
        "nextCardExpiryDate": "00/00/0000",
        "firstCardVerifyDate": "00/00/0000",
        "statusChangeDate": "13/01/2023",
        "cardActivatedDate": "17/04/2023"
    },
    "warningCodeDetails": {
        "warningCode1": "0",
        "warningCode1SetDate": "00/00/0000",
        "warningCode7": "0"
    },
    "blockCodeDetails": {
        "blockSecurityId": "",
        "blockDate": "00/00/0000",
        "blockCode": ""
    },
    "paymentInstrumentId": "0009543162000007495",
    "businessUnit": 700,
    "status": "0",
    "currentCardNeedActivation": "N",
    "lastCardActivation": "N",
    "productId": 2,
    "numberOfCardsOutstanding": 1,
    "cardReturnedCount": 0,
    "cardAction": "0",
    "cardRequestedCount": 0,
    "cardType": 0,
    "cardTypeRequested": 0,
    "isSecureCodeEnabled": "0",
    "visaPlusIndicator": "0",
    "customerId": "8844564501141032",
    "posServiceCode": "101",
    "cardholderType": "1",
    "pinDelayDaysCount": 0,
    "visaMiniCardVersion": "0",
    "isPinSuppressionEnabled": "0",
    "reissueAttemptCount": 0,
    "fraudCardTransferCount": "",
    "cardReissueDeliveryLocation": 0,
    "cardReissueDeliveryOption": "0",
    "firstIssueBranch": 0,
    "authorizationCriteriaTableId": "",
    "emblemId": 0,
    "cardDelayDaysCount": 0,
    "customersGender": "0",
    "reasonCode": "",
    "pinOverride": "1",
    "mobileDeviceID": "",
    "mobileProvisionStatus": "0",
    "digitalId": "",
    "plasticId": "",
    "maskedPaymentCardNumber": "000431683XXXXXX9609",
    "externalContractId": "12345678912341",
    "transferToPaymentInstrumentId": "",
    "isDynamicCVV2Enabled": "0",
    "transferFromPaymentInstrumentId": "",
    "physicalVirtualIndicator": "P",
    "accountId": "0007000022606063500"
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
