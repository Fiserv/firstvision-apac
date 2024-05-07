# Inquire Account Plan

This API is used to fetch the plan details for a given account Id like status, interest table override details, plan level balances, dues and dates etc.

## Endpoint

`GET /v1/accounts/{accountId}/inquirePlan`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "businessUnit": 200,
  "accountId": "0002000010000400044",
  "planSequenceNumber": 1,
  "beginningBalance": "$0.00",
  "disputedAmount": "$0.00",
  "billedNotPaidDetails": {
    "interestAmount": "$0.00",
    "serviceFeeAmount": "$0.00",
    "lateFeeAmount": "$0.00",
    "annualFeeAmount": "$0.00",
    "overlimitFeeAmount": "$0.00",
    "insuranceAmount": "$0.00",
    "recoveryFeeAmount": "$0.00",
    "collectionFeeAmount": "$0.00",
    "nsfFeeAmount": "$0.00",
    "userFee1Amount": "$0.00",
    "userFee2Amount": "$0.00",
    "userFee3Amount": "$0.00",
    "userFee4Amount": "$0.00",
    "userFee5Amount": "$0.00",
    "userFee6Amount": "$0.00",
    "principalAmount": "$0.00"
  },
  "dateFieldsDetails": {
    "planDate": "01/03/2021",
    "interestAssessmentStartDate": "00/00/0000",
    "insuranceAssessmentStartDate": "00/00/0000",
    "accruedThroughDate": "31/12/2020",
    "billingBeginningDate": "00/00/0000",
    "paymentBeginningDate": "00/00/0000",
    "paidOutDate": "00/00/0000",
    "effectiveRateChangeDate": "00/00/0000",
    "effectiveDate": "01/03/2021",
    "paymentTypeIndicatorMaintenanceDate": "00/00/0000",
    "lastPaymentDate": "00/00/0000",
    "userFee1assessmentDate": "00/00/0000",
    "userFee2assessmentDate": "00/00/0000",
    "userFee3assessmentDate": "00/00/0000"
  },
  "generalDetails": {
    "planDescription": " ",
    "referenceNumber": " ",
    "multipleSales": "Y",
    "consolidatedPayment": "N",
    "consolidatedStatement": "Y",
    "limitIndicator": 0,
    "rateType": " "
  },
  "interestTableOverrideDetails": {
    "tableId": 0,
    "expiryDate": "00/00/0000",
    "status": " "
  },
  "miscellenousDetails": {
    "rateTableOccurrenceIndicator": 2,
    "lastInterestRateTableUsed": 0,
    "balanceTransferMonthsRemaining": 0,
    "disclosureDays": 0,
    "userdefinedProductCode": "10002",
    "userdefinedPromotionalProductId": " ",
    "lastPurchaseBalanceAmount": "$1.00",
    "lifeToDateReturnAmount": "$0.00",
    "lifeToDateRequestedPaymentAmount": "$0.00",
    "lifeToDateAppliedPaymentAmount": "$0.00",
    "previousFixedPaymentAmount": "$0.00",
    "interestExpiryDisclosureIndicator": 0,
    "cycleToDatePostedPaymentAmount": "$0.00",
    "paymentType": "T",
    "fixedPaymentAmount": "$0.00",
    "lastRequestedPaymentAmount": "$0.00",
    "lastPaymentAmount": "$0.00",
    "planNumberForConsolidatedPayments": 10002
  },
  "lastInterestRate": "0.00000%",
  "planType": "R",
  "planStatus": 1,
  "previousPlanStatus": 0,
  "planStatusChangeDate": "00/00/0000",
  "planTotalDueAmount": "$0.00",
  "eligibleBalanceForStatementInstalment": "$10.00"
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
    "instance": "/v1/accounts/0002000010000400044/inquirePlan",
    "invalid-params": [
      "V5PS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/inquirePlan).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get Request - Record Not Found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
