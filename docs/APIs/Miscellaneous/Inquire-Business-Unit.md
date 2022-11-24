# Inquire Business Unit

This API is used to view functionality control switches available at organization level. Using this API, control switches can be managed effectively.

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
  "accruedCredit": 0,
  "accruedDebit": 0,
  "businessUnit": 600,
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
  "generalLedgerDetails": {
    "accountingMethod": "A",
    "batchNonPostedCreditReversals": "2",
    "batchNonPostedCredits": "2",
    "batchNonPostedDebitReversals": "1",
    "batchNonPostedDebits": "1",
    "businessUnitLevel": "Y",
    "defaultGlAccountForCredits": "4",
    "defaultGlAccountForDebits": "3",
    "generalLedgerReportingType": "D",
    "generatePlanLevelGlReporting": "N",
    "generateProductLevelGlReporting": "N",
    "nonPostedCreditPurges": "2",
    "nonPostedCreditReversals": "2",
    "nonPostedCredits": "2",
    "nonPostedDebitPurges": "1",
    "nonPostedDebitReversals": "1",
    "nonPostedDebits": "1"
  },
  "installmentLoansActive": "1",
  "loanCreditLimit": "$0.00",
  "loanLimitCalculationMethod": "A",
  "mccLimits": {
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
  "processingControls": {
    "actionOnFinanceCharge": "0",
    "actionOnLateFee": "0",
    "addUnpaidMinAmountDueBalances": "0",
    "allowConsolidatedPayments": "1",
    "autoChargebackActive": "0"
  },
  "relationshipAuthorisationActive": "1",
  "todaysDate": "18/08/2021",
  "transactionBasedOffers": "0",
  "useServiceCharges": "Y"
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
| `businessUnit` | Query Parameter | *number* | 03 | Unique identification number associated with the organization. Valid values from 001-998.|


### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get request - Record Not Found |  
| `V5PS4009SA` | Org not present on file |  
| `V5PS4010SA` | Account is not present not on file | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*