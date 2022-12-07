# Inquire Product

This service provides product details for a given product number. Products are primary control records that gives client option to enable or disable various functionalities like Card activation, PIN mailer, Loan feature, Collections, Loyalty, Falcon, Alerts etc. 
  
## Endpoint

`GET /v1/products/{productId}/details`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Business Unit and Plan id should be sent as query parameters and path variable.*** 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/products/{productId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 001-998. |
| `productId` | Path Variable | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 001-998. | 

### Successful Response Payload

```json
{
  "authAlerts": "0",
  "automaticAccountNumberGeneration": "I",
  "businessUnit": 600,
  "cardActivationControls": {
    "additionalCardActivation": "Y",
    "newCardActivation": "Y",
    "reissueCardActivation": "Y",
    "replacementCardActivation": "Y"
  },
  "cardMailerNameaddress": "0",
  "cardProductDisplay": "0",
  "creditLimitBypass": "0",
  "defaultCardTechnology": "3",
  "delinquencyAgeing": "D",
  "embossingFilesKeyType": "B",
  "enhancedProductsEligible": "0",
  "includeDisputedAmounts": "1",
  "isCardActionTableEnabled": "0",
  "isCardBureauFeedbackEnabled": "0",
  "isCardPresenttransactionEnabled": "",
  "isChipOrPinCardEnabled": "1",
  "isCollectionsEnabled": "Y",
  "isCrossBorderAlertEnabled": "0",
  "isDebitCardProcessEnabled": "0",
  "isDirectDebitCreditEnabled": "Y",
  "isFalcon6Enabled": "0",
  "isLoanFeatureEnabled": "1",
  "isLocalorInternationalUsageEnabled": "0",
  "isLoyaltyManagementEnabled": "1",
  "isManualPinResetEnabled": "1",
  "isNewCardDefaultEnabled": "0",
  "isOverlimitProcessingOptinIndicatorEnabled": "0",
  "isPaymentHolidaysEnabled": "Y",
  "isSameDayEmbossingEnabled": "0",
  "isScriptingEnabled": "0",
  "isSecureCodeEnabled": "0",
  "isSweepOptionEnabled": "0",
  "isTokenizationServiceEnabled": "1",
  "isVipOverrideEnabled": "N",
  "isWspTokenEnabled": "-16",
  "issuanceId": "SX1",
  "keyTypeForPinMailerFiles": "B",
  "markUpFeeEnabled": {
    "isIssuerEnabled": "0",
    "isReimburseIssuerOrSchemaEnabled": "0",
    "isSchemeEnabled": "0",
    "isUserDefinedEnabled": "0"
  },
  "newCardPlastics": "Y",
  "openToBuyCreditBalance": "3",
  "paymentProcessingControls": {
    "applicationMethodForAccountReceivable": "H",
    "applicationMethodForProfitLoss": "D",
    "paymentApplicationLevel": "P",
    "prepaymentsAllowed": "0"
  },
  "pinMailerForCardAction": [
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    },
    {
      "cardAction": "0",
      "pinOptions": "0"
    }
  ],
  "pinMailerNameaddress": "0",
  "processingControlLevel": "O",
  "productDescription": "VISA CREDIT CONSUMER",
  "productId": 1,
  "quarterlyAffiliateCardProduct": "V1",
  "residenceId": "SX1",
  "typeOfAccount": "X"
}
```

### Error Response Payload

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

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |         
| `V5CR0004SF` | Get request - Record not found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
