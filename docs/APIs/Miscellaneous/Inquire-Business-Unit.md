# Inquire Business Unit

This API is used to fetch parameters defined at business unit. Business unit are primary control records that gives client option to enable or disable various functionalities like MCC limits, Loan active, general ledger etc. Business units establishes operating parameters for companies that process accounts in a similar fashion.s

## Endpoint

`GET /v1/misc/{businessUnit}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Business Unit should be sent as query parameter.***

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "businessUnitName": "NAB",
  "countryCode": "AUS",
  "currencyCode": 36,
  "businessUnitRegion": "1",
  "todaysDate": "18/08/2021",
  "nextProcessingDate": "19/08/2021",
  "interestAccruedThroughDate": "18/08/2021",
  "lastMaintenanceDate": "18/08/2021",
  "generalLedgerDetails": {
    "businessUnitLevel": "Y",
    "generateProductLevelGlReporting": "Y",
    "generatePlanLevelGlReporting": "Y",
    "accountingMethod": "A",
    "nonPostedDebits": " ",
    "nonPostedDebitReversals": " ",
    "nonPostedDebitPurges": " ",
    "batchNonPostedDebits": " ",
    "batchNonPostedDebitReversals": " ",
    "defaultGlAccountForDebits": " ",
    "nonPostedCredits": " ",
    "nonPostedCreditReversals": " ",
    "nonPostedCreditPurges": "Y",
    "batchNonPostedCredits": " ",
    "batchNonPostedCreditReversals": " ",
    "defaultGlAccountForCredits": " ",
    "generalLedgerReportingType": "D"
  },
  "accruedDebit": 1234,
  "accruedCredit": 1235,
  "transactionBasedOffers": "1",
  "useServiceCharges": "Y",
  "processingControls": {
    "allowConsolidatedPayments": "0",
    "addUnpaidMinAmountDueBalances": "0",
    "autoChargebackActive": "0",
    "actionOnLateFee": "0",
    "actionOnFinanceCharge": "0"
  },
  "commercialCardsAllowed": "1",
  "relationshipAuthorisationActive": "",
  "cashCreditLimitCalculationMethod": "A",
  "cashCreditLimit": "$100,000.00",
  "loanLimitCalculationMethod": "A",
  "loanCreditLimit": "$0.00",
  "excludeDefaultDisputedAmounts": "0",
  "mccLimits": {
    "mccLimitAmount1": "$0.00",
    "mccLimitAmount2": "$0.00",
    "mccLimitAmount3": "$0.00",
    "mccLimitAmount4": "$0.00",
    "mccLimitAmount5": "$0.00",
    "mccLimitAmount6": "$0.00",
    "mccLimitAmount7": "$0.00",
    "mccLimitAmount8": "$0.00",
    "mccLimitAmount9": "$0.00",
    "mccLimitAmount10": "$0.00"
  },
  "earlySettlementQuotesProcess": "0",
  "installmentLoansActive": "0",
  "isBnplEnabled": 1
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
    "instance": "/v1/misc/900/details",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/misc/{businessUnit}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 03 | Unique identification number associated with the organization. Valid values from 1-998.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get request - Record Not Found |  
| `V5PS4009SA` | Org not present on file |  
| `V5PS4010SA` | Account is not present not on file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
