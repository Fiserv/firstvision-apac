# Board Entities

This new API enables to choose the records you want to add (Customer Name/Address record, Account Base Segment record, Embosser record, and Relationship record), then prompts you to provide a valid values for required field that correspond to the records you selected.

## Endpoint

`POST /v1/misc/boardEntities`

## Payload Example

### Request Payload

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
      "postalCode": ""
    }
  }
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/misc/boardEntities).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `baseAccountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `isCustomerIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new customer record. |
| `createAccountRecord` | Payload | *string* | 01 | This is the code that indicates whether to add a new account record. |
| `isSameCustomerIdAccountIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether CUSTOMER NUMBER and BASE ACCOUNT NUMBER are to be the same number. |
| `isRelationshipEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new Relationship record. |
| `isPaymentInstrumentIdEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add a new Embosser record. |
| `businessUnit` | Payload | *number* | 03 | Identification number of the business unit associated with the  account. |
| `productId` | Payload | *number* | 03 | Identification number of the product associated with the account or relationship. |
| `isInsuranceProductEnabled` | Payload | *string* | 01 | This is the code that indicates whether to add an Insurance Product record. |
| `givenName` | Payload | *string* | 40 | First name of the customer. |
| `billingCycle` | Payload | *number* | 02 | Billing cycle of the account associated with the customer. |
| `creditLimit` | Payload | *number* | 17 | Credit limit of this account. |
| `billingCycle` | Payload | *number* | 02 | Billing cycle of the relationship associated with the customer. |
| `owningBranchNumber` | Payload | *number* | 9 | This field is the number of the branch that owns this account and location of financial reporting for this account. |
| `isSuppressLetterEnabled` | Payload | *number* | 01 | Code that indicates whether to suppress all letters for the account. |
| `isAnnualMembershipFeeEnabled` | Payload | *number* | 01 | Flag that indicates whether to waive the annual membership fee for the account. |
| `isSupressTokenEnabled` | Payload | *string* | 01 | Token suppression at account level indicator. |
| `coreBankingIndicator` | Payload | *string* | 01 | This is the code indicates type of banking. |
| `paymentInstrumentId` | Payload | *string* | 19 | Unique alternate identification number associated with Payment card number. |
| `embossedName1` | Payload | *string* | 26 | This field that specifies the default generic name line 1. |
| `cardholderFlag` | Payload | *string* | 01 | This is the code that indicates whether the card is issued as primary or secondary card. |
| `deviceIndicator` | Payload | *string* | 01 | Code that indicates the type of device (form factor) written to
the track data on the card. |

### Successful Response Payload

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

### Error Response Payload

```json
{
   errorCode" :  V5SB4003EA" ,
   errorMessage" : Base account number required"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4003EA` | Base account number required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer na account must be blank |
| `V5SB4005EB` | Customer na account required |
| `V5SB4005EG` | Customer na account must be blank |
| `V5SB4005EH` | Customer na account must be numeric |
| `V5SB4008EA` | Relationship not valid for this org |
| `V5SB4008EB` | Relationship not valid for the dual org |
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |
| `V5SB4157EC` | Account nbr exist on relationship file for this org |
| `V5SB4157ED` | Account nbr exist on relationship file for dual org |
| `V5SB4158EA` | Account nbr cannot duplicate existing embosser for this org |
| `V5SB4158EB` | Account nbr cannot duplicate existing embosser for dual org |
| `V5SB4151EA` | Logo does not allow billing account generation |
| `V5SB4151EB` | Maximum number of 20 attempts made on billing account |
| `V5SB4151EC` | Generated account number is greater than ending billing number |
| `V5SB4151ED` | Logo does not allow account number generation |
| `V5SB4151EE` | Maximum number of 20 attempts made on base account number |
| `V5SB4151EG` | Generated account number is greater than base ending number |
| `V5SB4152EB` | Org does not allow account number generation |
| `V5SB4160EA` | Invalid base account check digit for this org |
| `V5SB4160EB` | Invalid base account number for this org |
| `V5SB4160EC` | Invalid base account check digit for dual org |
| `V5SB4160ED` | Invalid base account number for dual org |
| `V5SB4003EA` | Base account number required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer na account must be blank |
| `V5SB4005EB` | Customer na account required |
| `V5SB4005EG` | Customer na account must be blank |
| `V5SB4005EH` | Customer na account must be numeric |
| `V5SB4008EA` | Relationship not valid for this org |
| `V5SB4008EB` | Relationship not valid for the dual org |
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |
| `V5SB4154SA` | Customer number not on file for this org |
| `V5SB4154SB` | Customer number already exists for this org |
| `V5SB4154SC` | Customer nbr must not be generic for personalized prepaid acct |
| `V5SB4154SD` | Generic customer not allowed |
| `V5SB4155EA` | Customer number not on file for the dual org |
| `V5SB4155EB` | Generic customer not allowed |
| `V5SB4155EC` | Customer number already exists for the dual org |
| `V5SB4154EA` | Invalid customer number |
| `V5SB4160EE` | Invalid customer check digit for this org |
| `V5SB4160EG` | Invalid customer check digit for dual org |
| `V5SB4003EA` | Base account number required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer na account must be blank |
| `V5SB4005EB` | Customer na account required |
| `V5SB4005EG` | Customer na account must be blank |
| `V5SB4005EH` | Customer na account must be numeric |
| `V5SB4008EA` | Relationship not valid for this org |
| `V5SB4008EB` | Relationship not valid for the dual org |
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid accounts |
| `V5SB4150EI` | No embosser records allowed for control accounts |
| `V5SB4150EJ` | No embosser records allowed for diversion accounts |
| `V5SB4150EK` | No embosser records allowed for billing accounts |
| `V5AP4061EA` | Number cards required must equal zero or 1 |
| `V5AP4063EA` | Embossed name type must not equal 3 |
| `V5AP4088EA` | Card delay days value must be numeric |
| `V5AP4097SA` | Card nbr and account nbr must be equal for card scheme |
| `V5AP4101SA` | Card number check digit is invalid |
| `V5AP4105SA` | Card sequence already at maximum for card number |
| `V5AP4106SA` | Card sequence already at maximum for chip card number |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*