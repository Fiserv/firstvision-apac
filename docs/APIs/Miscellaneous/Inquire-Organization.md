# Inquire Organization

This API is used to view functionality control switches available at organization level. Using this API, control switches can be managed effectively.

## Endpoint

`GET /v1/misc/{orgNumber}/orgDetails`

## Payload Example

### Request Payload

>Should be empty.
>
>***The Business Unit should be sent as query parameter.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/misc/{orgNumber}/orgDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `orgNumber` | Payload | *number* | 03 | Identification number of the business unit. The values are 000–998.|

### Successful Response Payload

```json

{
  "accruedCredit": 0,
  "accruedDebit": 0,
  "billingCyclAssignmentsRes": {
    "billingCyclAssignment10Res": {
      "dateOfLastStatement10": "",
      "nextCycleCallDay10": "0"
    },
    "billingCyclAssignment11Res": {
      "dateOfLastStatement11": "",
      "nextCycleCallDay11": "0"
    },
    "billingCyclAssignment12Res": {
      "dateOfLastStatement12": "",
      "nextCycleCallDay12": "0"
    },
    "billingCyclAssignment13Res": {
      "dateOfLastStatement13": "",
      "nextCycleCallDay13": "0"
    },
    "billingCyclAssignment14Res": {
      "dateOfLastStatement14": "",
      "nextCycleCallDay14": "0"
    },
    "billingCyclAssignment15Res": {
      "dateOfLastStatement15": "",
      "nextCycleCallDay15": "0"
    },
    "billingCyclAssignment16Res": {
      "dateOfLastStatement16": "",
      "nextCycleCallDay16": "0"
    },
    "billingCyclAssignment17Res": {
      "dateOfLastStatement17": "",
      "nextCycleCallDay17": ""
    },
    "billingCyclAssignment18Res": {
      "dateOfLastStatement18": "",
      "nextCycleCallDay18": ""
    },
    "billingCyclAssignment19Res": {
      "dateOfLastStatement19": "",
      "nextCycleCallDay19": ""
    },
    "billingCyclAssignment1Res": {
      "dateOfLastStatement1": "",
      "nextCycleCallDay1": "0"
    },
    "billingCyclAssignment20Res": {
      "dateOfLastStatement20": "",
      "nextCycleCallDay20": ""
    },
    "billingCyclAssignment21Res": {
      "dateOfLastStatement21": "",
      "nextCycleCallDay21": ""
    },
    "billingCyclAssignment22Res": {
      "dateOfLastStatement22": "",
      "nextCycleCallDay22": ""
    },
    "billingCyclAssignment23Res": {
      "dateOfLastStatement23": "",
      "nextCycleCallDay23": ""
    },
    "billingCyclAssignment24Res": {
      "dateOfLastStatement24": "",
      "nextCycleCallDay24": ""
    },
    "billingCyclAssignment25Res": {
      "dateOfLastStatement25": "",
      "nextCycleCallDay25": ""
    },
    "billingCyclAssignment26Res": {
      "dateOfLastStatement26": "",
      "nextCycleCallDay26": ""
    },
    "billingCyclAssignment27Res": {
      "dateOfLastStatement27": "",
      "nextCycleCallDay27": ""
    },
    "billingCyclAssignment28Res": {
      "dateOfLastStatement28": "",
      "nextCycleCallDay28": ""
    },
    "billingCyclAssignment29Res": {
      "dateOfLastStatement29": "",
      "nextCycleCallDay29": ""
    },
    "billingCyclAssignment2Res": {
      "dateOfLastStatement2": "",
      "nextCycleCallDay2": "0"
    },
    "billingCyclAssignment30Res": {
      "dateOfLastStatement30": "",
      "nextCycleCallDay30": ""
    },
    "billingCyclAssignment31Res": {
      "dateOfLastStatement31": "00/00/0000",
      "nextCycleCallDay31": "31"
    },
    "billingCyclAssignment3Res": {
      "dateOfLastStatement3": "",
      "nextCycleCallDay3": "0"
    },
    "billingCyclAssignment4Res": {
      "dateOfLastStatement4": "",
      "nextCycleCallDay4": "0"
    },
    "billingCyclAssignment5Res": {
      "dateOfLastStatement5": "",
      "nextCycleCallDay5": "0"
    },
    "billingCyclAssignment6Res": {
      "dateOfLastStatement6": "",
      "nextCycleCallDay6": "0"
    },
    "billingCyclAssignment7Res": {
      "dateOfLastStatement7": "",
      "nextCycleCallDay7": "0"
    },
    "billingCyclAssignment8Res": {
      "dateOfLastStatement8": "",
      "nextCycleCallDay8": "0"
    },
    "billingCyclAssignment9Res": {
      "dateOfLastStatement9": "",
      "nextCycleCallDay9": "0"
    }
  },
  "businessUnitName": "FISERV DEMO ORG",
  "businessUnitRegion": "4",
  "cashCreditLimit": "$100,000.00",
  "cashCreditLimitCalculationMethod": "P",
  "commercialCardsAllowed": "2",
  "countryCode": "AUS",
  "currencyCode": 36,
  "dateInterestAccruedThrough": "18/08/2021",
  "dateLastMaintenance": "08/10/2021",
  "dateNextProcess": "19/08/2021",
  "earlySettlementQuotesProcess": "1",
  "excludeDefaultDisputedAmounts": "1",
  "generalLedgerDetailsRes": {
    "accountingMethod": "A",
    "batchNonpostCreditReversals": "2",
    "batchNonpostDebitReversals": "1",
    "batchNonpostedCredits": "2",
    "batchNonpostedDebits": "1",
    "businessUnitLevel": "Y",
    "defaultGlAccountForCredits": "4",
    "defaultGlAccountForDebits": "3",
    "generalLedgerReportingType": "D",
    "generatePlanLevelGlReporting": "N",
    "generateProductLevelGlReporting": "N",
    "nonpostedCreditPurges": "2",
    "nonpostedCreditReversals": "2",
    "nonpostedCredits": "2",
    "nonpostedDebitPurges": "1",
    "nonpostedDebitReversals": "1",
    "nonpostedDebits": "1"
  },
  "installmentLoansActive": "1",
  "loanCreditLimit": "$0.00",
  "loanLimitCalculationMethod": "A",
  "mccLimitsRes": {
    "mccLimitAmount1": "$999,999,999.99",
    "mccLimitAmount10": "$0.00",
    "mccLimitAmount2": "$999,999,999.99",
    "mccLimitAmount3": "$999,999,999.99",
    "mccLimitAmount4": "$999,999,999.99",
    "mccLimitAmount5": "$999,999,999.99",
    "mccLimitAmount6": "$999,999,999.99",
    "mccLimitAmount7": "$999,999,999.99",
    "mccLimitAmount8": "$0.00",
    "mccLimitAmount9": "$0.00"
  },
  "orgNumber": 600,
  "processingControlsRes": {
    "actionOnFinanceCharge": "0",
    "actionOnLateFee": "0",
    "addUnpaidMinAmountDueBalances": "0",
    "allowConsolidatedPayments": "1",
    "autoChargebackActive": "0"
  },
  "relationshipAuthorisationActive": "1",
  "todaysDate": "18/08/2021",
  "transactionBasedOffers": 0,
  "useServiceCharges": "Y"
}

```

### Error Response Payload

```json
{
   errorCode" :  V5PH0004SF" ,
   errorMessage" : Get Request - Record Not Found"   
}
```
Below table provides the list of application's error code and its description.

| `V5PH0004SF` | Get Request - Record Not Found |  
| `V5PS4009SA` | Org not present on file |
| `V5PS4010SA` | Account is not present not on file | 