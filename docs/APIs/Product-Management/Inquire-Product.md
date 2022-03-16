# Inquire Product

This service provides product details for a given product number. Products are primary control records that gives client option to enable or disable various functionalities like Card activation, PIN mailer, Loan feature, Collections, Loyalty, Falcon, Alerts etc. 
  
## Endpoint

`GET /v1/products/{productNumber}/details`

## Payload Example

### Request Payload

>Should be empty.
***The Business Unit and Plan Number should be sent as query parameters and path variable.*** 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](..api/?type=get&path=/v1/products/{productNumber}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Business Unit - Identification number associated with this account base segment record, the values are 001–998 |
| `productNumber` | Path Variable | *number* | 3 | Product - This field is the identification number of the Logo record | 

### Successful Response Payload

```json
{
  "additionalCardActivation": "Y",
  "applicationMethodForAr": "H",
  "applicationMethodForPl": "D",
  "approvedCardUse": "0",
  "authAlerts": "0",
  "automaticAccountNumberGeneration": "I",
  "businessUnit": 600,
  "cardActionTableActive": "0",
  "cardBureauFeedbackActive": "0",
  "cardMailerNameaddress": "0",
  "cardProductDisplay": "0",
  "chippinCardAllowed": "1",
  "collectionsActive": "Y",
  "creditLimitBypass": "0",
  "crossBorder": "0",
  "debitCardProcessActive": "0",
  "defaultCardTechnology": "3",
  "delinquencyAgeing": "D",
  "directDebitcreditActive": "Y",
  "embossingFilesKeyType": "B",
  "enhancedProductsEligible": "0",
  "falcon6Active": "0",
  "includeDisputedAmounts": "1",
  "keyTypeForPinMailerFiles": "B",
  "loanFeatureActive": "1",
  "loyaltyManagementActive": "1",
  "manualPinResetAllowed": "1",
  "markupActiveCreditFee": "0",
  "markupIssuerActive": "0",
  "markupSchemeActive": "0",
  "markupUserDefinedActive": "0",
  "newCardActivation": "Y",
  "newCardDefaultActive": "0",
  "newCardPlastics": "Y",
  "openToBuyCreditBalance": "3",
  "overlimitProcessingOptinIndicator": "0",
  "paymentApplicationLevel": "P",
  "paymentHolidaysAllowed": "Y",
  "pinMailerForCardAction": [
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    },
    {
      "cardActions": "0",
      "pinOptions": "0"
    }
  ],
  "pinMailerNameaddress": "0",
  "prepaymentsAllowed": "0",
  "processingControlLevel": "O",
  "productDescription": "VISA CREDIT CONSUMER",
  "productNumber": 1,
  "quarterlyAffiliateCardProduct": "V1",
  "reissueCardActivation": "Y",
  "replacementCardActivation": "Y",
  "sameDayEmboss": "0",
  "sameDayEmbossingAllowed": "0",
  "scriptingActive": "0",
  "secureCodeActive": "0",
  "stateOfIssueId": "SX1",
  "stateOfResidenceId": "SX1",
  "sweepOptionAllowed": "0",
  "tokenizationServiceActive": "1",
  "typeOfAccountsProcessed": "X",
  "vipOverrideFlag": "N",
  "virtualCardEdits": "",
  "wspTokenEligible": "-16"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5CR0004SF",
  "errorMessage": "Get Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CR0484EA` | Org not found |         
| `V5CR0004SF` | Get Request - Record not found | 