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
>***The Business Unit and product id should be sent as query parameters and path variable.***

<!--
type: tab
-->

```json
{
    "pinMailerForCardAction": [
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        },
        {
            "pinOptions": 0,
            "cardAction": "0"
        }
    ],
    "markUpFeeEnabled": {
        "isReimburseIssuerOrSchemaEnabled": "0",
        "isIssuerEnabled": "0",
        "isSchemeEnabled": "1",
        "isUserDefinedEnabled": "0"
    },
    "cardActivationControls": {
        "reissueCardActivation": "N",
        "replacementCardActivation": "N",
        "newCardActivation": "N",
        "additionalCardActivation": "N"
    },
    "paymentProcessingControls": {
        "applicationMethodForAccountReceivable": "K",
        "applicationMethodForProfitLoss": "K",
        "prepaymentsAllowed": 0,
        "paymentApplicationLevel": "P"
    },
    "bnplAlerts": {
        "isbookingAlertEnabled": 1,
        "bookingAlertChannelIndicator": 3,
        "isIplanActivationAlertEnabled": 1,
        "iplanActivateAlertChannelIndicator": 3,
        "isPaymentDueAlertEnabled": 1,
        "paymentDueAlertChannelIndicator": 1,
        "isMissPamyemtAlertEnabled": 1,
        "missPaymentAlertChannelIndicator": 3,
        "isSwitchAlertEnabled": 1,
        "switchAlertChannelIndicator": 3,
        "isSnoozeAlertEnabled": 1,
        "snoozeAlertChannelIndicator": 3
    },
    "bnplDetails": {
        "isBnplEnabled": 1,
        "configurationTemplate": "BNPLBUD44",
        "isRecalculatePayDateEnabled": 0,
        "repaymentIndicator": 1,
        "repaymentDays": 1,
        "paymentGraceDays": 1,
        "missedPaymentCount": 3,
        "missedPaymentBlockCode": "A",
        "isSnoozeEnabled": 1,
        "snoozeCount": 3,
        "offerSwitchMethod": 1,
        "offerSwitchCount": 3
    },
    "bnplTierRangeOfTemplateId": [
        {
            "configurationTemplate": "BNPL24",
            "tierMinimumAmount": "$5.00",
            "tierMaximumAmount": "$100.00"
        },
        {
            "configurationTemplate": "BNPLBUD44",
            "tierMinimumAmount": "$101.00",
            "tierMaximumAmount": "$200.00"
        },
        {
            "configurationTemplate": "BNPLBUN08",
            "tierMinimumAmount": "$201.00",
            "tierMaximumAmount": "$300.00"
        },
        {
            "configurationTemplate": "BNPLBUN09",
            "tierMinimumAmount": "$301.00",
            "tierMaximumAmount": "$400.00"
        },
        {
            "configurationTemplate": "BNPLBUD44",
            "tierMinimumAmount": "$401.00",
            "tierMaximumAmount": "$600.00"
        }
    ],
    "typeOfAccount": "X",
    "isLocalorInternationalUsageEnabled": 0,
    "cardProductDisplay": 0,
    "businessUnit": 700,
    "productId": 2,
    "isLoyaltyManagementEnabled": "0",
    "isDirectDebitCreditEnabled": "Y",
    "productDescription": "BNPL VISA CREDIT CARDS",
    "quarterlyAffiliateCardProduct": "V1",
    "isLoanFeatureEnabled": 0,
    "isPaymentHolidaysEnabled": "N",
    "isSameDayEmbossingEnabled": 0,
    "isChipOrPinCardEnabled": 1,
    "delinquencyAgeing": "S",
    "processingControlLevel": "O",
    "isCollectionsEnabled": "N",
    "automaticAccountNumberGeneration": "I",
    "isOverlimitProcessingOptionIndicatorEnabled": 0,
    "openToBuyCreditBalance": 3,
    "includeDisputedAmounts": 1,
    "residenceId": "B01",
    "issuanceId": "B01",
    "isWspTokenEnabled": 1,
    "authAlerts": 0,
    "isFalcon6Enabled": "0",
    "isVipOverrideEnabled": "Y",
    "isSecureCodeEnabled": 0,
    "isDebitCardProcessEnabled": 0,
    "isTokenizationServiceEnabled": 1,
    "isManualPinResetEnabled": 1,
    "isCardActionTableEnabled": 0,
    "defaultCardTechnology": 3,
    "isScriptingEnabled": 1,
    "isSweepOptionEnabled": 0,
    "isCrossBorderAlertEnabled": 0,
    "creditLimitBypass": 0,
    "isNewCardDefaultEnabled": 0,
    "enhancedProductsEligible": 0,
    "isCardPresenttransactionEnabled": "X",
    "physicalVirtualIndicator": "",
    "newCardPlastics": "Y",
    "embossingFilesKeyType": "B",
    "keyTypeForPinMailerFiles": "B",
    "pinMailerNameaddress": 0,
    "cardMailerNameaddress": 0,
    "isCardBureauFeedbackEnabled": 0
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
