# Build Dashboard

Using the following recipe, the issuing banks' digital application can build a nice widgets providing cards and accounts details linked to customer. 

---

- [Step 1: Generate OAuth Token](#step-1-generate-oauth-token)
- [Step 2: List cards and Accounts](#step-2-list-cards-accounts)
- [Step 3: Fetch Account Details](#step-3-account-details)
- [Step 4: Fetch Card Details](#step-4-card-details)
- [Step 5: Build Dashboard](#step-5-build-dashboard)

---

## Step 1: Generate OAuth Token

Get the Oauth token.

  `GET /v1/api/oauth/token?grant_type=client_credentials&scope=cards+misc`

```json
{
"access_token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImVkaXQiLCJjbGllbnRfaWQiOiJQT0NfTkFCX0RldiIsImZpcnN0VmlzaW9uSWQiOiIwMDAwMEFVTkFCIiwiZXhwIjoxNzUwMzkyMDAwfQ.uWiSQfLLzfDYuSmPwmLa1fVx6Vyw8Rtphv49uo_2EbfoJYzppHNscar8NWNEp4sXHdxbrEmftu_JJ3oTLD8AtbNgQh9ej8lUEvfA8vbYM3ucXuOC1NWxZPD7tDiwQ6kLypsYgbOhBMQ_U7Icobbh2I9o1Zit8F9xT7J70e3ZLJqtqTWC1WDd0WmOG672KpU_tc2eMtUvLYqrMKjRr2KuD-e73fc27zdYpeL9GElVlo1WKbrHOvsdolr92mvhHBf_etnQ5Pb_X_x533-DiT1piCkjBTqZqgd6cdV2ItdPVAz8CfwmjS6TJR95B3Ys9Xp3tdI5UwP3NmkaYRqP5_R02Q",
"expires_in": 1750392000,
"token_type": "Bearer"
}
```

<!-- theme: info -->
> Use the access token in all the subsequent calls.

## Step 2: List cards and Accounts using external-id

Using the external-id (for example - SSN ID/ Driving License / Passport Number), fetch the cards and accounts associated with the customer.  

  `GET /v1/customers/{externalCustomerId}/listExternalCustomersCardsAndAccounts`

```json
{
    "accountList": {
        "blockCode2": "",
        "shortName": "SRAVANTHI",
        "residenceId": "B01",
        "totalCardsCount": 3,
        "businessUnit": 700,
        "productId": 1,
        "accountId": "0007000011925283501",
        "status": "N",
        "memoDebitAmount": "0.00",
        "blockCode1": "",
        "addressId": "12"
    },
    "cardList": [
        {
            "paymentInstrumentId": "0009543161000021084",
            "blockCode1": " ",
            "embossedName": "SRAVANTHI9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/06/2025"
        },
        {
            "paymentInstrumentId": "0009543161000021126",
            "blockCode1": " ",
            "embossedName": "SRAVANTHI9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/04/2025"
        },
        {
            "paymentInstrumentId": "0009543161000023601",
            "blockCode1": " ",
            "embossedName": "chsrabc9916",
            "addressId": "C9916",
            "plasticId": " ",
            "expiryDate": "28/10/2025"
        }
    ],
    "externalCustomerId": "99993499789916"
}
```

## Step 3: Fetch Account Details

Using the account number fetch in the previous API, call the below service to get more details of the accounts.  

  `GET /v1/accounts/{accountId}/details`

```json
{
  "accountId": "0002000010000403266",
  "addressId": "",
  "alternateCustomerIdDetails": {
    "customerId": "0000000000000000000",
    "customerIdEffectiveDate": "00/00/0000",
    "customerIdExpiryDate": "00/00/0000",
    "customerIdFlag": ""
  },
  "amountDetails": {
    "actualDirectDebitPaymentAmount": "$0.00",
    "cashAvailable": "$0.00",
    "cashBalance": "$0.00",
    "cashCreditLimit": "$0.00",
    "creditLimit": "$0.00",
    "currentBalance": "$0.00",
    "currentDueAmount": "$0.00",
    "cycleToDatePaymentAmount": "$0.00",
    "firstPurchaseAmount": "$0.00",
    "highBalanceAmount": "$0.00",
    "immediateDueAmount": "$0.00",
    "incomeAmount": "$0.00",
    "lastCashAdvancedAmount": "$0.00",
    "lastPaymentAmount": "$0.00",
    "lastPurchaseAmount": "$0.00",
    "loanAvailable": "$0.00",
    "loanBalance": "$0.00",
    "loanCreditLimit": "$0.00",
    "memoCreditAmount": "$0.00",
    "memoDebitAmount": "$0.00",
    "openToBuy": "$0.00",
    "pastDueAmount": "$0.00",
    "projectedDdAmount": "$0.00",
    "totalDueAmount": "$0.00"
  },
  "billingAcctInd": "0",
  "billingCycle": 31,
  "billingLevel": "1",
  "blockCodeDetails": {
    "blockCode1": "",
    "blockCode1Date": "00/00/0000",
    "blockCode2": "",
    "blockCode2Date": "00/00/0000"
  },
  "businessUnit": 200,
  "chargeOffDetails": {
    "additionalChargeOffReason": "",
    "chargeOffDaysCount": 0,
    "chargeOffReason": "",
    "chargeOffStatus": "0",
    "resetChargeoffDaysSwitch": "0"
  },
  "correspondenceCustomerId": "",
  "currencyCode": "36",
  "customerId": "0002000002000007799",
  "dateFieldsDetails": {
    "accountClosedDate": "00/00/0000",
    "accountOpenDate": "17/08/2021",
    "cardFeeDate": "00/00/0000",
    "firstPurchaseDate": "00/00/0000",
    "graceDayExpireDate": "00/00/0000",
    "greatestExpiryDate": "16/08/2024",
    "lastCashAdvancedDate": "00/00/0000",
    "lastCreditDate": "00/00/0000",
    "lastDayToAuthorizeDate": "00/00/0000",
    "lastDebitDate": "00/00/0000",
    "lastPaymentDate": "00/00/0000",
    "lastPurchaseDate": "00/00/0000",
    "lastStatementDate": "31/07/2021",
    "nextCreditIntPaymentDate": "00/00/0000",
    "nextStatementDate": "31/08/2021",
    "notificationReceivedDate": "00/00/0000",
    "paymentDueDate": "00/00/0000"
  },
  "deferMembershipFeeDate": "00/00/0000",
  "disputedDetails": {
    "cashDisputedAmout": "$0.00",
    "cashDisputedItemsCount": 0,
    "disputedItemsCount": 0,
    "totalCashDisputedItemsAmount": "$0.00"
  },
  "employeeCode": "",
  "externalCustomerId": "",
  "isFraudulentReportEnabled": "N",
  "isRestructureEnabled": "N",
  "isVipEnabled": "0",
  "issuanceId": "SX1",
  "letterRequest": "",
  "liabilityIndicator": "0",
  "numberOfUnblockedCards": 2,
  "pctOverrideDetails": {
    "pctExpiryDate": "00/00/0000",
    "pctOverride": "",
    "pctStartDate": "00/00/0000"
  },
  "permanentCollector": "",
  "primaryAccountFlag": "",
  "relationshipId": "",
  "residenceId": "SX1",
  "returnMailCount": 0,
  "returnMailDate": "00/00/0000",
  "returnMailUser": "",
  "shortName": "TESTING",
  "sourceCode": "",
  "status": "D",
  "userAccountId": "0000000000000000000"
}
```

## Step 4: Fetch Card Details

Using the payment instrument ID fetched in the step 2 above, call the below service to get more details of the card associated with customer.  

  `GET /v1/cards/{paymentInstrumentId}/details`

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
  "cardAction": "1",
  "cardDelayDaysCount": 0,
  "cardReissueDeliveryLocation": 0,
  "cardReissueDeliveryOption": "5",
  "cardRequestedCount": 1,
  "cardReturnedCount": 0,
  "cardType": 0,
  "cardTypeRequested": 0,
  "cardholderType": "1",
  "currentCardNeedActivation": "N",
  "customerId": "",
  "customersGender": "0",
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
  "externalCustomerId": "",
  "firstIssueBranch": 0,
  "fraudCardTransferCount": "",
  "isDynamicCVV2Enabled": "",
  "isPinSuppressionEnabled": "0",
  "isSecureCodeEnabled": "0",
  "lastCardActivation": "N",
  "mobileDeviceID": "",
  "mobileProvisionStatus": "0",
  "nameFields": {
    "cardholderName1": "",
    "cardholderName2": "",
    "embossedName1": "R0203 CARDHOLDER#3",
    "name1TypeIndicator": "0",
    "name2TypeIndicator": "0",
    "embossedName2": "FISERV DEMO FACILITY"
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
  "userDefinedFields": {
    "field1": "",
    "field2": "",
    "field3": "",
    "field4": 0,
    "field5": ""
  },
  "visaMiniCardVersion": "0",
  "visaPlusIndicator": "0",
  "warningCodeDetails": {
    "warningCode1": "1",
    "warningCode1SetDate": "18/08/2021",
    "warningCode7": "0"
  }
} 
```

## Step 4: Build Dashboard with Cards and Accounts Details

Using the above details, banks' can build a nice mobile application widgets providing the comprehensive view of the customer's accounts and the cards details.

## See also

- [Generate OAuth Token](?path=docs/APIs/Security/get-access-token.md)
- [List cards and Accounts](?path=docs/APIs/Customer-Management/List-External-Customer-Cards-And-Accounts.md)
- [Fetch Account Details](?path=docs/APIs/Account-Management/Inquire-Account.md)
- [Fetch Card Details](?path=docs/APIs/Card-Management/Inquire-Card.md)

---
