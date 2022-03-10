# Inquire Card

This service is used to retrive detailed information of card. This API response provides information about card demogrpahic and processing parameters. 

## Endpoint

`GET /v1/cards/{cardNumber}/details`

## Payload Example

### Request Payload

>Shoud be empty.  
***The Business Unit and Card Number should be sent as query parameters and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/details).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "cardholderType": 0,
  "businessUnit": 600,
  "lastCardExpirationDate": "01/02/2020",
  "cardIssueDate": "01/02/2020",
  "lastCardActivation": "N",
  "postalCode": " ",
  "pinOverride": "string",
  "typeOfCardRequested": 0,
  "secureCodeActiveForAccount": 0,
  "firstIssueBranch": 0,
  "spendingLimitPrepaymentAvailable": "$0.00",
  "visaMiniCardVersion": 0,
  "dateFirstCardVerify": "01/02/2020",
  "maximumAmountRetailAuthorizationsAllowed": "$1,000.00",
  "addressLine1": " ",
  "addressLine2": " ",
  "currentChipSequenceNumber": 0,
  "mailerDate": "01/02/2020",
  "mobileProvisionStatus": "string",
  "emblem": 0,
  "authorizationCriteriaTableIdNumber": " ",
  "cardReissueDeliveryOption": 0,
  "blockDate": "25/01/202",
  "blockSecurityId": " ",
  "name1TypeIndicator": 0,
  "cardholderName1": " ",
  "digitalId": "string",
  "cardholderName2": " ",
  "name2TypeIndicator": 0,
  "maximumNumberRetailAuthorizationsAllowed": 999999999,
  "stateProvince": " ",
  "maximumNumberOtcAuthorizationsAllowed": 999999999,
  "cardReissueDeliveryLocation": 0,
  "warningBulletinDistributionRegion": " ",
  "secureIdStatusChanged": "C1X",
  "maximumAmountSingleAtmTransactionAllowed": "$2,000.00",
  "languageIndicator": " ",
  "embosserRecordStatus": 0,
  "maximumAuthorizationsFrequnecy": 1,
  "cardDelayDays": 0,
  "cardNumber": 9544410000000062,
  "statusDateChange": "01/02/2020",
  "transferEffectiveDate": "01/02/2020",
  "spendingLimitPrepaymentAmount": "$0.00",
  "city": " ",
  "spendingCategoryStatistics": [
    {
      "spendingCategoryNumberLtd1": 999999999,
      "spendingCategoryAmountToday1": 0,
      "spendingCategoryNumberCtd1": 999999999,
      "spendingCategoryNumberToday1": 999999999,
      "spendingCategoryAmountCtd1": "$1,000.00",
      "spendingCategoryAmountYtd1": "$1,000.00",
      "spendingCategoryNumberYtd1": 999999999,
      "spendingCategoryAmountLtd1": "$1,000.00",
      "spendingCategoryNumberWtd1": 999999999,
      "spendingCategoryAmountWtd1": "$1,000.00"
    }
  ],
  "dateCurrentCardValid": "string",
  "maximumNumberAtmCashAuthorizationsAllowed": 999999999,
  "singleOtcCashAuthorizationAllowed": "$0.00",
  "mobileDeviceId": "string",
  "currentCardNeedActivation": "N",
  "nameOnCard": "DAVID TEST 2",
  "nameOn2ndLine": " ",
  "spendingLimitPrepaymentExpiryDate": "01/02/2020",
  "posServiceCode": " ",
  "fraudCardTransferNumber": " ",
  "maximumAmountAtmCashAuthorizationsAllowed": "$1,000.00",
  "cardsReturnedForEmbosser": 0,
  "reasonCode": "string",
  "issuingAttemptsRemaining": 0,
  "pinOffset": 0,
  "cardActivatedDate": "19/08/2021",
  "expirationDate": "16/08/2024",
  "userdefinedField5": " ",
  "maximumAmountOtcCashAuthorizationsAllowed": "$1,000.00",
  "userdefinedField4": 0,
  "product": 0,
  "blockCode": " ",
  "numberOfCardsOutstanding": 1,
  "typeOfCard": 0,
  "authorizationSpendingLimits": [
    {
      "frequency1": 0,
      "number1": 5,
      "maximum1": 0
    }
  ],
  "customersGender": "string",
  "warningCode7": 0,
  "typeOfMailer": " ",
  "pinDelayDays": 0,
  "customerNumber": " ",
  "userdefinedField1": " ",
  "postToAccountNumber": 6000022000000076,
  "userdefinedField3": " ",
  "warningCode1": 0,
  "userdefinedField2": " ",
  "previousPinOffset": 0,
  "singleRetailAuthorizationAllowed": "$999,999,999,999,999.99",
  "authorizationAccumulators": [
    {
      "accumulatedAuthorizationAmountCtd1": "$10234.00",
      "accumulatedAuthorizationAmountYtd1": "$123456.00",
      "accumulatedAuthorizationAmountToday1": "$1000.00",
      "accumulatedAuthorizationNumberToday1": 5,
      "accumulatedAuthorizationNumberCtd1": 6,
      "accumulatedAuthorizationNumberYtd1": 8,
      "accumulatedAuthorizationAmountLtd1": "$1234560.00",
      "accumulatedAuthorizationNumberLtd1": 12
    }
  ],
  "pinMailerSuppression": 0,
  "visaPlusIndicator": 0,
  "cardAction": 1,
  "numberOfCardsRequested": 1,
  "warningBulletinLastDate": "01/02/2020",
  "nextCardExpirationDate": "01/02/2020",
  "previousChipSequenceNumber": 0
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4001EC",
  "errorMessage": "Dual org not found or add pending"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EC` | Dual ORG not found or add pending |
|`V5ED4001ER` | Bin NBR should be same for account and card |
|`V5ED4001ES` | Dual org not found or add pending |
|`V5ED4001SA` | ORG not found |
|`V5ED4001SB` | ORG is in add pending |
|`V5ED4001SC` | ORG is in purged |
|`V5ED4001SD` | Account not present |
|`V5ED4001SE` | Logo not present |
|`V5ED4001SF` | Invalid ORG |
|`V5ED4001EJ` | Record not found |
|`V5ED4001EL` | Record not found |
|`V5ED4001EN` | Record purged or add pending |
|`V5ED4002EA` | Invalid card number |
|`V5ED4002ED` | Card number must be provided |
|`V5ED4002ES` | Card number must be equal to post to account NBR |
|`V5ED4002ER` | BIN NBR should be same for both account and card |
|`V5ED4002EE` | Invalid check digit - card number |
|`V5ED4003EA` | Invalid sequence number |
|`V5ED4003ED` | Card seq number must be greater than zero |
|`V5ED4003EQ` | Post to acct for dual org not on file |
|`V5ED4003EW` | Invalid rec number for this account |
|`V5ED4003EX` | HCS system active and node record not found |
|`V5ED9910ED` | Post to acct invalid check digit |
|`V5ED9910EF` | Post to acct record not found |