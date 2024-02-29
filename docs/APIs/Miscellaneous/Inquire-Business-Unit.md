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
    "generalLedgerDetails": {
        "batchNonPostedCredits": "1",
        "batchNonPostedDebitReversals": "1",
        "businessUnitLevel": "Y",
        "generalLedgerReportingType": "D",
        "generatePlanLevelGlReporting": "N",
        "nonPostedCreditReversals": "1",
        "batchNonPostedDebits": "1",
        "accountingMethod": "A",
        "nonPostedDebits": "1",
        "nonPostedDebitReversals": "1",
        "nonPostedDebitPurges": "1",
        "defaultGlAccountForDebits": "1",
        "nonPostedCredits": "1",
        "nonPostedCreditPurges": "1",
        "generateProductLevelGlReporting": "N",
        "batchNonPostedCreditReversals": "1",
        "defaultGlAccountForCredits": "1"
    },
    "processingControls": {
        "autoChargebackActive": 0,
        "allowConsolidatedPayments": 1,
        "actionOnFinanceCharge": 0,
        "actionOnLateFee": 0,
        "addUnpaidMinAmountDueBalances": 0
    },
    "mccLimits": {
        "mccLimitAmount1": "100.00",
        "mccLimitAmount2": "0.00",
        "mccLimitAmount3": "0.00",
        "mccLimitAmount4": "0.00",
        "mccLimitAmount5": "0.00",
        "mccLimitAmount6": "0.00",
        "mccLimitAmount7": "0.00",
        "mccLimitAmount8": "0.00",
        "mccLimitAmount9": "0.00",
        "mccLimitAmount10": "0.00"
    },
    "instalmentDetails": {
        "isExpandDescriptionEnabled": "Y",
        "isInstalmentsEnabled": "1",
        "isConversionEnabledForCancelledInstalments": "0",
        "memoTransactionCode": 819
    },
    "instalmentTransactionCodeDetails": [
        {
            "transactionDescription": "EPP CONV-$$($T)",
            "transactionCode": 38303
        },
        {
            "transactionDescription": "EPP CONVERSION DEBIT",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI FEE FOR $$($T)",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI PROCESSING FEE-C",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EPP FORECLOSURE PRINCIPAL CREDIT",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI FORECLOSURE PRINCIPAL DEBIT",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI FORECLOSURE INTEREST CREDIT",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI FORECLOSURE INTEREST DEBIT",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI FORECLOSURE FEE",
            "transactionCode": 38323
        },
        {
            "transactionDescription": " ",
            "transactionCode": 38323
        },
        {
            "transactionDescription": "EMI CANCELLATION PRINCIPAL DEBIT",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EMI CANCELLATION INTEREST CREDIT",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EMI CANCELLATION INTEREST DEBIT",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EPP PRINCIPAL REVERSAL",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EMI FOR $$ ($C/$T)",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EMI INT-$$ ($C/$T)",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "EMI PROCESSING FEE REVERSAL",
            "transactionCode": 38333
        },
        {
            "transactionDescription": "00000000000000",
            "transactionCode": 0
        }
    ],
    "businessUnit": 700,
    "accruedDebit": 0,
    "businessUnitName": "NAB BANKING SERVICE LTD1",
    "countryCode": "AUS",
    "currencyCode": 36,
    "businessUnitRegion": "4",
    "lastMaintenanceDate": "10/11/2023",
    "transactionBasedOffers": 0,
    "installmentLoansActive": 1,
    "earlySettlementQuotesProcess": 1,
    "commercialCardsAllowed": 0,
    "interestAccruedThroughDate": "30/09/2024",
    "nextProcessingDate": "01/10/2024",
    "todaysDate": "30/09/2024",
    "useServiceCharges": "Y",
    "excludeDefaultDisputedAmounts": 0,
    "cashCreditLimitCalculationMethod": "A",
    "cashCreditLimit": "0.00",
    "loanLimitCalculationMethod": "A",
    "loanCreditLimit": "0.00",
    "relationshipAuthorisationActive": "0",
    "isBnplEnabled": 4,
    "accruedCredit": 0
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
