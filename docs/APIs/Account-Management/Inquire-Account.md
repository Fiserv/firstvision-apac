# Inquire Account

The service provides the basic details of the account associated with the customer. Some basic details include short name, credit limit, billing cycle etc.

## Endpoint

`GET /v1/accounts/{accountId}/details`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Successful Response Payload

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

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/000200001000040329A/details",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found|

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*