# Inquire Product

This API is used to fetch details for a given product Id. Products are primary control records that gives client option to enable or disable various functionalities like Card activation, PIN mailer, Loan feature, Collections, Loyalty, Falcon, Alerts etc.
  
## Endpoint

`GET /v1/products/{productId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Business Unit and Plan id should be sent as query parameters and path variable.***

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "productId": 1,
  "productDescription": "VISA CREDIT CONSUMER",
  "cardProductDisplay": "0",
  "quarterlyAffiliateCardProduct": "V1",
  "isLoanFeatureEnabled": "1",
  "isPaymentHolidaysEnabled": "Y",
  "isSameDayEmbossingEnabled": "1",
  "isChipOrPinCardEnabled": "1",
  "delinquencyAgeing": "D",
  "processingControlLevel": "O",
  "isCollectionsEnabled": "Y",
  "automaticAccountNumberGeneration": "I",
  "authAlerts": "0",
  "isFalcon6Enabled": "0",
  "isVipOverrideEnabled": "N",
  "isSecureCodeEnabled": "0",
  "isLoyaltyManagementEnabled": "1",
  "isDebitCardProcessEnabled": "0",
  "isTokenizationServiceEnabled": "1",
  "isManualPinResetEnabled": "1",
  "isCardActionTableEnabled": "0",
  "defaultCardTechnology": "3",
  "isScriptingEnabled": "0",
  "isSweepOptionEnabled": "0",
  "isCrossBorderAlertEnabled": "0",
  "creditLimitBypass": "0",
  "isLocalorInternationalUsageEnabled": "0",
  "isNewCardDefaultEnabled": "0",
  "enhancedProductsEligible": "0",
  "isCardPresenttransactionEnabled": " ",
  "newCardPlastics": "Y",
  "embossingFilesKeyType": "B",
  "keyTypeForPinMailerFiles": "B",
  "pinMailerNameaddress": "0",
  "cardMailerNameaddress": "0",
  "isCardBureauFeedbackEnabled": "0",
  "pinMailerForCardAction": [
    {
      "cardAction": "0",
      "pinOptions": "0"
    }
  ],
  "isDirectDebitCreditEnabled": "N",
  "isOverlimitProcessingOptinIndicatorEnabled": "0",
  "openToBuyCreditBalance": "1",
  "includeDisputedAmounts": "0",
  "residenceId": "SX1",
  "issuanceId": "SX1",
  "isWspTokenEnabled": "1",
  "typeOfAccount": "X",
  "markUpFeeEnabled": {
    "isReimburseIssuerOrSchemaEnabled": "0",
    "isIssuerEnabled": "0",
    "isSchemeEnabled": "0",
    "isUserDefinedEnabled": "0"
  },
  "cardActivationControls": {
    "newCardActivation": "Y",
    "additionalCardActivation": "Y",
    "reissueCardActivation": "Y",
    "replacementCardActivation": "Y"
  },
  "paymentProcessingControls": {
    "applicationMethodForAccountReceivable": "H",
    "applicationMethodForProfitLoss": "D",
    "prepaymentsAllowed": "0",
    "paymentApplicationLevel": "P"
  },
  "bnplAlerts": {
    "isbookingAlertEnabled": 0,
    "bookingAlertChannelIndicator": 0,
    "isIplanActivationAlertEnabled": 0,
    "iplanActivateAlertChannelIndicator": 0,
    "isPaymentDueAlertEnabled": 0,
    "paymentDueAlertChannelIndicator": 0,
    "isMissPamyemtAlertEnabled": 0,
    "missPaymentAlertChannelIndicator": 0,
    "isSwitchAlertEnabled": 0,
    "switchAlertChannelIndicator": 1,
    "isSnoozeAlertEnabled": 0,
    "snoozeAlertChannelIndicator": 0
  },
  "bnplDetails": {
    "isBnplEnabled": 0,
    "configurationTemplate": "BNPLTMPL10",
    "isRecalculatePayDateEnabled": 1,
    "repaymentIndicator": 0,
    "repaymentDays": 1,
    "paymentGraceDays": 1,
    "missedPaymentCount": 2,
    "missedPaymentBlockCode": " ",
    "isSnoozeEnabled": 0,
    "snoozeCount": 0,
    "offerSwitchMethod": 0,
    "offerSwitchCount": 0
  },
  "bnlplTierRangeOfTemplateId": [
    {
      "configurationTemplate": "TEMPLATE 1",
      "tierMinimumAmount": "0000000001000",
      "tierMaximumAmount": "0000000010000"
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
    "instance": "/v1/products/290/details",
    "invalid-params": [
      "V5CR0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Path Variable | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |
| `V5CR0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
