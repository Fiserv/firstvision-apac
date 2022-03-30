# Inquire Card

This service is used to retrive detailed information of card. This API response provides information about card demogrpahic and processing parameters. 

## Endpoint

`GET /v1/cards/{cardNumber}/details`

## Payload Example

### Request Payload

>Should be empty.  
***The Card Number should be sent as path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{cardNumber}/details).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |

### Successful Response Payload

```json
{
  "addressLine1": "FISERV",
  "addressLine2": "NAB",
  "authorizationAccumulatorsRes": [
    {
      "accumulatedAuthorizationAmountCTD": "$0.00",
      "accumulatedAuthorizationAmountLTD": "$0.00",
      "accumulatedAuthorizationAmountToday": "$0.00",
      "accumulatedAuthorizationAmountYTD": "$0.00",
      "accumulatedAuthorizationNumberCTD": 0,
      "accumulatedAuthorizationNumberLTD": 0,
      "accumulatedAuthorizationNumberToday": 0,
      "accumulatedAuthorizationNumberYTD": 0
    },
    {
      "accumulatedAuthorizationAmountCTD": "$0.00",
      "accumulatedAuthorizationAmountLTD": "$0.00",
      "accumulatedAuthorizationAmountToday": "$0.00",
      "accumulatedAuthorizationAmountYTD": "$0.00",
      "accumulatedAuthorizationNumberCTD": 0,
      "accumulatedAuthorizationNumberLTD": 0,
      "accumulatedAuthorizationNumberToday": 0,
      "accumulatedAuthorizationNumberYTD": 0
    },
    {
      "accumulatedAuthorizationAmountCTD": "$0.00",
      "accumulatedAuthorizationAmountLTD": "$0.00",
      "accumulatedAuthorizationAmountToday": "$0.00",
      "accumulatedAuthorizationAmountYTD": "$0.00",
      "accumulatedAuthorizationNumberCTD": 0,
      "accumulatedAuthorizationNumberLTD": 0,
      "accumulatedAuthorizationNumberToday": 0,
      "accumulatedAuthorizationNumberYTD": 0
    }
  ],
  "authorizationCriteriaTableIdNumber": "800",
  "authorizationSpendingLimitsRes": [
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    },
    {
      "frequency": "0",
      "maximum": 0,
      "number": 0
    }
  ],
  "blockCode": "X",
  "blockDate": "19/08/2021",
  "blockSecurityId": "NAB",
  "businessUnit": 600,
  "cardAction": "1",
  "cardActivatedDate": "00/00/0000",
  "cardDelayDays": 0,
  "cardIssueDate": "00/00/0000",
  "cardNumber": "0009544410000000047",
  "cardReissueDeliveryLocation": 0,
  "cardReissueDeliveryOption": "5",
  "cardholderName1": "",
  "cardholderName2": "",
  "cardholderType": "1",
  "cardsReturnedForEmbosser": 0,
  "city": "CHENNAI",
  "currentCardNeedActivation": "N",
  "currentChipSequenceNumber": 0,
  "customerNumber": "",
  "customersGender": "0",
  "dateCurrentCardValid": "00/00/0000",
  "dateFirstCardVerify": "00/00/0000",
  "digitalId": "",
  "emblem": 0,
  "embosserRecordStatus": "0",
  "expirationDate": "17/08/2024",
  "firstIssueBranch": 0,
  "fraudCardTransferNumber": "",
  "issuingAttemptsRemaining": 0,
  "languageIndicator": "",
  "lastCardActivation": "N",
  "lastCardExpirationDate": "00/00/0000",
  "mailerDate": "00/00/0000",
  "maximumAmountAtmCashAuthorizationsAllowed": "$1,000.00",
  "maximumAmountOtcCashAuthorizationsAllowed": "$1,000.00",
  "maximumAmountRetailAuthorizationsAllowed": "$1,000.00",
  "maximumAmountSingleAtmTransactionAllowed": "$2,000.00",
  "maximumAuthorizationsFrequnecy": "1",
  "maximumNumberAtmCashAuthorizationsAllowed": 999999999,
  "maximumNumberOtcAuthorizationsAllowed": 999999999,
  "maximumNumberRetailAuthorizationsAllowed": 999999999,
  "mobileDeviceID": "",
  "mobileProvisionStatus": "0",
  "name1TypeIndicator": "0",
  "name2TypeIndicator": "0",
  "nameOn2ndLine": "FISERV DEMO FACILITY",
  "nameOnCard": "R0203 CARDHOLDER#3",
  "nextCardExpirationDate": "00/00/0000",
  "numberOfCardsOutstanding": 0,
  "numberOfCardsRequested": 1,
  "pinDelayDays": 0,
  "pinMailerSuppression": "0",
  "pinOffset": 0,
  "pinOverride": "1",
  "posServiceCode": "",
  "postToAccountNumber": "0006000022000000050",
  "postalCode": "",
  "previousChipSequenceNumber": 0,
  "previousPinOffset": 0,
  "product": 2,
  "reasonCode": "",
  "secureCodeActiveForAccount": "0",
  "secureIdStatusChanged": "",
  "singleOtcCashAuthorizationAllowed": "$0.00",
  "singleRetailAuthorizationAllowed": "$999,999,999,999,999.99",
  "spendingCategoryStatisticsRes": [
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    },
    {
      "spendingCategoryAmountCTD": "$0.00",
      "spendingCategoryAmountLTD": "$0.00",
      "spendingCategoryAmountToday": 0,
      "spendingCategoryAmountWTD": "$0.00",
      "spendingCategoryAmountYTD": "$0.00",
      "spendingCategoryNumberCTD": 0,
      "spendingCategoryNumberLTD": 0,
      "spendingCategoryNumberToday": 0,
      "spendingCategoryNumberWTD": 0,
      "spendingCategoryNumberYTD": 0
    }
  ],
  "spendingLimitPrepaymentAmount": "$0.00",
  "spendingLimitPrepaymentAvailable": "$0.00",
  "spendingLimitPrepaymentExpiryDate": "00/00/0000",
  "stateProvince": "",
  "statusDateChange": "00/00/0000",
  "transferEffectiveDate": "00/00/0000",
  "typeOfCard": 0,
  "typeOfCardRequested": 0,
  "typeOfMailer": "",
  "userdefinedField1": "",
  "userdefinedField2": "",
  "userdefinedField3": "",
  "userdefinedField4": 0,
  "userdefinedField5": "",
  "visaMiniCardVersion": "0",
  "visaPlusIndicator": "0",
  "warningBulletinDistributionRegion": "",
  "warningBulletinLastDate": "00/00/0000",
  "warningCode1": "1",
  "warningCode7": "0"
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