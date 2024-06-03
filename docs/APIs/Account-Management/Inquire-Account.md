# Inquire Account

The API provides the basic details of an account associated with the customer. Some basic details include short name, credit limit, billing cycle, balances, statement dates etc.

## Endpoint

`GET /v1/accounts/{accountId}/details`

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
  "accountId": "0002000010000403266",
  "productId": 1,
  "billingAcctInd": 0,
  "shortName": "Dhruv",
  "customerId": "0002000002000007799",
  "alternateCustomerIdDetails": {
    "customerIdFlag": "A",
    "customerIdExpiryDate": "15/04/2022",
    "customerId": "0000000001000000065",
    "customerIdEffectiveDate": "14/01/2021"
  },
  "blockCodeDetails": {
    "blockCode1": "A",
    "blockCode2": "X",
    "blockCode1Date": "10/01/2021",
    "blockCode2Date": "10/02/2021"
  },
  "dateFieldsDetails": {
    "accountOpenDate": "10/06/2006",
    "accountClosedDate": "00/00/0000",
    "nextStatementDate": "26/05/2022",
    "cardFeeDate": "26/05/2021",
    "notificationReceivedDate": "00/00/0000",
    "lastDayToAuthorizeDate": "00/00/0000",
    "paymentDueDate": "06/06/2022",
    "lastPaymentDate": "00/00/0000",
    "lastDebitDate": "10/04/2022",
    "lastCreditDate": "00/00/0000",
    "firstPurchaseDate": "20/02/2007",
    "greatestExpiryDate": "31/12/2030",
    "nextCreditIntPaymentDate": "00/00/0000",
    "lastStatementDate": "26/04/2022",
    "lastPurchaseDate": "10/05/2022",
    "graceDayExpireDate": "00/00/0000",
    "lastCashAdvancedDate": "00/00/0000",
    "creditLimitChangeDate": "19/08/2021"
  },
  "amountDetails": {
    "creditLimit": "$10000.00",
    "openToBuy": "$10000.00",
    "currentBalance": "$0.00",
    "currentDueAmount": "$120.00",
    "totalDueAmount": "$0.00",
    "immediateDueAmount": "$0.00",
    "memoCreditAmount": "$0.00",
    "memoDebitAmount": "$0.00",
    "cashCreditLimit": "$0.00",
    "cashBalance": "$0.00",
    "cashAvailable": "$0.00",
    "firstPurchaseAmount": "$0.00",
    "lastPaymentAmount": "$0.00",
    "cycleToDatePaymentAmount": "$2000.00",
    "loanCreditLimit": "$0.00",
    "loanBalance": "$0.00",
    "loanAvailable": "$0.00",
    "projectedDdAmount": "$0.00",
    "actualDirectDebitPaymentAmount": "$0.00",
    "highBalanceAmount": "$1450.00",
    "incomeAmount": "$5000.00",
    "pastDueAmount": "$0.00",
    "lastPurchaseAmount": "$100.00",
    "balanceTransferOutstandingAmount" : "$0.00",
    "lastCashAdvancedAmount": "$0.00"
  },
  "userAccountId": " ",
  "status": "A",
  "billingCycle": 26,
  "isRestructureEnabled": "Y",
  "numberOfUnblockedCards": 2,
  "relationshipId": " ",
  "billingLevel": 1,
  "isVipEnabled": 0,
  "liabilityIndicator": 0,
  "employeeCode": " ",
  "returnMailCount": 0,
  "returnMailUser": " ",
  "returnMailDate": "00/00/0000",
  "permanentCollector": " ",
  "correspondenceCustomerId": " ",
  "letterRequest": " ",
  "isFraudulentReportEnabled": "N",
  "chargeOffDetails": {
    "chargeOffStatus": 0,
    "chargeOffReason": " ",
    "resetChargeoffDaysSwitch": 0,
    "additionalChargeOffReason": " ",
    "chargeOffDaysCount": 0
  },
  "disputedDetails": {
    "disputedItemsCount": 0,
    "totalCashDisputedItemsAmount": "$0.00",
    "cashDisputedAmount": "$0.00",
    "cashDisputedItemsCount": 0
  },
  "deferMembershipFeeDate": "00/00/0000",
  "residenceId": "SX1",
  "issuanceId": "SX1",
  "primaryAccountFlag": "P",
  "externalContractId": "0000000000012672379",
  "addressId": "HOME",
  "sourceCode": " ",
  "excludeFromVAUOrABUIndicator": 0,
  "pctOverrideDetails": {
    "pctExpiryDate": "31/12/2025",
    "pctStartDate": "29/01/2022",
    "pctOverride": "HCS"
  },
  "statementDeliveryMode": "E",
  "bnplDetails": {
    "ConfigurationTemplate": "TMPL1",
    "lastIplanSequenceNumber": 0,
    "missedPaymentCount": 2,
    "snoozeCount": 0,
    "switchCount": 0
  }
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

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
