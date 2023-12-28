# Inquire Plan Controls

This API is used to fetch loan plan details for a given plan Id.
  
## Endpoint

`GET /v1/loans/{planId}/controls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***The Business Unit and Plan id should be sent as query parameters and path variable.***

<!--
type: tab
-->

```json
{
    "instalmentConversionFeeControls": {
        "feeIndicator": "2",
        "amountOrPercentage": "120000",
        "planIndicator": "0"
    },
    "loanCancellationControls": {
        "isReverseUserFee2Enabled": 0,
        "isReverseUserFee3Enabled": 0,
        "isReverseUserFee4Enabled": 0,
        "isReverseUserFee5Enabled": 0,
        "isReverseUserFee6Enabled": 0,
        "timePeriod": 0,
        "isPaymentByCancelEnabled": 0,
        "isReverseInterestEnabled": 0,
        "isReverseInsuranceEnabled": 0,
        "isReverseLateFeeEnabled": 0,
        "isReverseOverlimitFeeEnabled": 0,
        "isReverseNonSufficientFundsEnabled": 0,
        "isReversMembershipFeeEnabled": 0,
        "isReverseServiceFeeEnabled": 0,
        "isReverseUserFee1Enabled": 0
    },
    "cciControls": {
        "interestIndicator": 0,
        "insuranceIndicator": 0,
        "userFee1Indicator": 0,
        "userFee2Indicator": 0,
        "userFee3Indicator": 0,
        "userFee4Indicator": 0,
        "userFee5Indicator": 0,
        "userFee6Indicator": 0
    },
    "instalmentControls": {
        "PaymentCreditBalanceIndicator": 0,
        "status": "2",
        "effectiveDate": "01/09/2023",
        "endingDate": "01/09/2025",
        "cycleDueAllowedForBooking": "7",
        "StatusAllowedForBooking": "00000000000000000000",
        "expiryDateIndicatorForBooking": "0",
        "transactionPostingIndicator": " ",
        "rollOverBalanceIndicator": 0,
        "rollOverPlanId": 0,
        "isLoanPlanTransferEnabled": 0,
        "isAdditionalInstalmentEnabled": 0,
        "rateOverrideIndicator": 1,
        "typeOfLoan": 1,
        "type": "1",
        "blockCodesAllowedForBooking": "000000000000000000000000000",
        "recalculationIndicator": "0",
        "minimumAmount": "$10.00",
        "maximumAmount": "$15,000.00",
        "postingPlanId": 0,
        "instalmentDescription": "TIP LOAN PLAN",
        "billedInstalmentDescription": "TEST 2"
    },
    "instalmentTenureControls": [
        {
            "tenure": 6,
            "annualPercentageRate": "0.00000%",
            "conversionFeeAmountOrPercentage": "$100.00"
        },
        {
            "tenure": 12,
            "annualPercentageRate": "0.00000%",
            "conversionFeeAmountOrPercentage": "$1,200.00"
        },
        {
            "tenure": 18,
            "annualPercentageRate": "0.00000%",
            "conversionFeeAmountOrPercentage": "$1,400.00"
        },
        {
            "tenure": 0,
            "annualPercentageRate": "0.00000%",
            "conversionFeeAmountOrPercentage": "$0.00"
        },
        {
            "tenure": 0,
            "annualPercentageRate": "0.00000%",
            "conversionFeeAmountOrPercentage": "$0.00"
        }
    ],
    "instalmentCancellationControls": {
        "status": "00000000000000000000",
        "blockCodes": "000000000000000000000000000",
        "cycleDue": "0"
    },
    "instalmentCloseFeeControls": {
        "feeIndicator": "0",
        "planIndicator": "0",
        "amount": "0"
    },
    "statementBilledNotPaidControls": {
        "interestIndicator": "N",
        "serviceFeeIndicator": "N",
        "lateFeeIndicator": "N",
        "membershipFeeIndicator": "N",
        "overlimitFeeIndicator": "N",
        "insuranceIndicator": "N",
        "recoveryFeeIndicator": "N",
        "collectionFeeIndicator": "N",
        "nonSufficientFundsFeeIndicator": "N",
        "userFee1Indicator": "N",
        "userFee2Indicator": "N",
        "userFee3Indicator": "N",
        "userFee4Indicator": "N",
        "userFee5Indicator": "N",
        "userFee6Indicator": "N",
        "principalIndicator": "N"
    },
    "endingDate": "31/12/2025",
    "beginningDate": "01/01/2012",
    "postingIndicator": 1,
    "paymentType": "C",
    "businessUnit": 700,
    "planId": 8,
    "multipleSalesIndicator": "Y",
    "description": "TIP EPP PLAN FEE BASED",
    "generateLoanReferenceNumber": 0,
    "autoGenerateTransactionToActivateLoan": 0,
    "planType": "L"
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
    "instance": "/v1/loans/8/controls",
    "invalid-params": [
      "V5CP0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{planId}/controls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number associated with this Account Base Segment entity, the values are 1–998. |
| `planId` | Path Variable | *number* | 5 | Identification number of the Credit Plan Master entity. The values are 1–99998. You can establish as many as 99,998 Credit Plan Master entities for each organization. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5CP0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
