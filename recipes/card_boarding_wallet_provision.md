# Card boarding to Wallet Provisioning of Digital Card

With the use of the Fiserv APIs, the issuing banks can improve the end-customer experience by digitally board a new card and instantly add the card to the ApplePay wallet.  

The issuing bank, after their risk assessment, can perform the following steps to allow customer to board a card and at the same time add them to Applepay Wallet.

---

- [Step 1: Generate OAuth Token](#step-1-generate-oauth-token)
- [Step 2: Board Entities](#step-2-board-entities)
- [Step 3: Activate Card](#step-3-activate-card)
- [Step 4: Add to Wallet](#step-4-add-to-wallet)

---

## Step 1: Generate OAuth Token

Get the Oauth token to make the subsequent API calls.
  `GET /v1/api/oauth/token?grant_type=client_credentials&scope=cards+misc`

## Step 2: Board Entities

This API will board all the required entities related to card boarding into the FirstVision applcation.

<!--
type: tab
titles: Request, Response
-->

```json
{
  "accountId": "/",
  "isCustomerIdEnabled": "Y",
  "createAccountRecord": "Y",
  "isSameCustomerIdAccountIdEnabled": "N",
  "isRelationshipEnabled": "N",
  "isPaymentInstrumentIdEnabled": "Y",
  "businessUnit": 600,
  "productId": 1,
  "customerId": "/",
  "relationshipNumber": "",
  "isInsuranceProductEnabled": "N",
  "customerDemographicDetails": {
    "dualFlag": "0",
    "title": "",
    "nameTypeIndicator1": "0",
    "nameTypeIndicator2": "0",
    "nameTypeIndicator3": "0",
    "residenceFlag": "1",
    "homePhone": "11230342",
    "employeePhone": "67894",
    "birthDate": "01/02/2010",
    "externalId": "",
    "gender": "1",
    "emailAddress": "",
    "alternateEmailAddress": "",
    "mobileNumber": "",
    "emailAddressFlag": "0",
    "addressDetails": {
      "addressLine1": "",
      "addressLine2": "",
      "city": "",
      "stateprovince": "",
      "postalCode": ""
    },
    "nameDetails": {
      "nameLine1": "",
      "nameLine2": "",
      "nameLine3": "",
      "birthName": "",
      "middleName": "",
      "givenName": "Tom"
    }
  },
  "relationshipDetails": {
    "relationshipCreditLimit": "",
    "relationshipBlockCode": " ",
    "mailCode": "0",
    "reserveAmountpctFlag": "0",
    "availableReservePctAmount": "",
    "isStatememtTypeEnabled": "0",
    "accountControlTableOverride": 0,
    "billingLevel": "1",
    "isBillingLevelModificationEnabled": "0",
    "defaultCreditLimit": "",
    "isCreditLimitModificationEnabled": "0",
    "corporateCustomerId": "",
    "customerGroupCode": "",
    "costCenterReportingNumber": "",
    "fiscalYearEnd": 0,
    "currentExpiryDate": "",
    "sourceCode": "",
    "contactName": "",
    "contactPhone": "",
    "officerName": "",
    "commercialFlag": "0",
    "authorizationCriteriaTable": "",
    "memoDetails": {
      "billingCurrency": 0,
      "paymentTransactionCode": 0,
      "paymentReversalTransactionCode": 0,
      "balanceIndicator": "0"
    },
    "feeDetails": {
      "annualFeeAssessmentLevel": "0",
      "isAnnualFeeModificationEnabled": "0",
      "lateFeeAssessmentLevel": "0",
      "isLateFeeModificationEnabled": "0",
      "nsfFeeAssessmentLevel": "0",
      "isNsfFeeModificationEnabled": "0"
    },
    "userDetails": {
      "userDate1": "",
      "userDate2": "",
      "userAmount1": "",
      "userAmount2": "",
      "userField5": "",
      "userField6": ""
    }
  },
  "accountDetails": {
    "corporateId": "",
    "primaryAccountFlag": " ",
    "shortName": "",
    "creditLimit": "1000",
    "billingCurrency": 0,
    "billingLevel": "1",
    "dualBillingFlag": "0",
    "customerSelectedDueDay": 0,
    "billingCycle": 18,
    "residenceId": "",
    "issuanceId": "600",
    "cashPlanId": 0,
    "retailPlanId": 0,
    "cardTechnology": "0",
    "temporaryCreditLimit": "0",
    "temporaryCreditLimitExpiryDate": "00/00/0000",
    "owningBranchNumber": 999999998,
    "isMobilePiEnabled": "0",
    "authorizationCriteriaTable": "",
    "isSuppressLetterEnabled": "0",
    "isWaiveAnnualMembershipFeeEnabled": "0",
    "isSupressTokenEnabled": "0",
    "coreBankingIndicator": " ",
    "externalCustomerId": "000012672302",
    "addressId": "HOME1",
    "sourceCode": "mbk2",
    "pctOverrideDetails": {
      "pctOverride": " ",
      "pctOverrideStartDate": "0",
      "pctOverrideExpiryDate": "0",
      "level": " ",
      "levelStartDate": "0",
      "levelExpiryDate": "0"
    },
    "ibsDetails": {
      "ddaRoutingId": 0,
      "ddaAccountId": "",
      "savingsRoutingId": 0,
      "savingsAccountId": ""
    }
  },
  "accountInsuranceProductData": {
    "dualIndicator": " ",
    "productCode": "",
    "statusCode": " ",
    "effectiveDate": "",
    "enrollId": "",
    "insuredPartyIndicator": "0",
    "premiumRate": 0,
    "ficheNumber": "",
    "source": "",
    "cancelReason": " ",
    "isMailLetterEnabled": "0",
    "isMailLetterFeeEnabled": "0",
    "mailStatement": "0"
  },
  "cardDetails": {
    "paymentInstrumentId": "/",
    "cardAction": "1",
    "numberOfCardsRequested": 0,
    "cardType": 0,
    "requestedCardType": 0,
    "cardMailerType": 0,
    "plasticId": "",
    "name1TypeIndicator": "0",
    "name2TypeIndicator": "0",
    "posServiceCode": 0,
    "cardholderFlag": "1",
    "visaMiniIndicator": "0",
    "programId": 0,
    "mobileDeviceId": "",
    "mobileProvisionStatus": "0",
    "deviceIndicator": "0",
    "mccGroupLimits": "",
    "chequeAccountId": "",
    "savingAccountId": "",
    "physicalVirtualIndicator": "V",
    "isDynamicCVV2Enabled": "0",
    "namesDetails": {
      "embossedName1": "Trump",
      "embossedName2": "",
      "name1": "",
      "name2": ""
    },
    "addressDetails": {
      "addressLine1": "",
      "addressLine2": "",
      "city": "",
      "stateprovince": "",
      "postalCode": "",
      "addressId": "C01"
    }
  }
}
```
<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "productId": 1,
  "customerId": "0006000012000000191",
  "relationshipId": "",
  "accountId": "0006000012000000191",
  "cardDetails": {
    "paymentInstrumentId": "0004440010910990851",
    "nameOnCard": "Trump",
    "expiryDate": "18/01/2024",
    "activationStatus": "0",
    "maskedPaymentCardNumber": ""
  }
}
```
<!-- type: tab-end -->

## Step 3: Activate Card

Activate the card after successful boarding of entities using above API.

<!--
type: tab
titles: Request, Response
-->

```json
{
  "currentCardNeedActivation": "N",
  "deactivateOldCard": "Y"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010273613",
  "currentCardNeedActivation": "N",
  "deactivateOldCard": "Y",
  "cardActivatedDate": "03/01/2020"
}
```
<!-- type: tab-end -->

## Step 4: Add to Wallet

The final step is to get the newly activated card to be added to the ApplePay wallet.  The push provisioning APIs can be used to generate the payload to initiate the green channel provisioning of newly created digital card on the ApplePay mobile-app.

<!--
type: tab
titles: Request, Response
-->

```json
{
  "identifier": "APPLE",
  "version": "1",
  "keysScheme": "FK",
  "ephemeralKey": "",
  "paymentInstrumentId": "0009644806050000069",
  "businessUnit": "100",
  "algorithm": "TDEA",
  "nonce": "123456"
} 
```

<!--
type: tab
-->

```json
{
  "provisionActivation": "MBPAC-1-FK-APPLE-  -TDEA-B0FAA81964D13652F1887E6ADCDEB2AB9CC237BA183DBAC47777692592551A3F57DF1C91E57909D5",
  "provisionAuthantication": "MBPAD-1-FK-APPLE-  -TDEA-59CBFFAE1E77B0DAE976CCABFEDBAD0EB778DC80163E09002DA60AF75FE04BFACD3070EE3FD8C6BCD2DE52D2D69D432B732D73AF95A32002D22C9F6257B7B"
}
```

<!-- type: tab-end -->

---

## See also

- [Generate OAuth Token](?path=docs/APIs/Security/get-access-token.md)
- [Board Entities](?path=docs/APIs/Miscellaneous/Board-Entities.md)
- [Activate Card](?path=docs/APIs/Card-Management/Activate-Card.md)
- [Add to Wallet](?path=docs/APIs/Card-Management/Push-Provisioning.md)

---
