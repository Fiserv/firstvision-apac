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
    "alternateCustomerIdDetails": {
        "customerId": "0000000000000000000",
        "customerIdEffectiveDate": "00/00/0000",
        "customerIdExpiryDate": "00/00/0000",
        "customerIdFlag": ""
    },
    "blockCodeDetails": {
        "blockCode1": "",
        "blockCode2": "",
        "blockCode1Date": "00/00/0000",
        "blockCode2Date": "00/00/0000"
    },
    "dateFieldsDetails": {
        "nextStatementDate": "18/09/2022",
        "cardFeeDate": "00/00/0000",
        "paymentDueDate": "09/09/2022",
        "lastPaymentDate": "00/00/0000",
        "lastDebitDate": "27/06/2022",
        "lastCreditDate": "00/00/0000",
        "firstPurchaseDate": "18/05/2022",
        "greatestExpiryDate": "31/05/2025",
        "nextCreditIntPaymentDate": "00/00/0000",
        "lastStatementDate": "26/08/2022",
        "graceDayExpireDate": "10/09/2022",
        "lastCashAdvancedDate": "00/00/0000",
        "lastPurchaseDate": "18/05/2022",
        "notificationReceivedDate": "00/00/0000",
        "accountClosedDate": "00/00/0000",
        "lastDayToAuthorizeDate": "00/00/0000",
        "accountOpenDate": "18/05/2022"
    },
    "amountDetails": {
        "openToBuy": "877.44",
        "currentBalance": "122.56",
        "totalDueAmount": "50.00",
        "immediateDueAmount": "25.00",
        "memoCreditAmount": "0.00",
        "memoDebitAmount": "0.00",
        "cashBalance": "0.00",
        "cashAvailable": "0.00",
        "firstPurchaseAmount": "2.00",
        "cycleToDatePaymentAmount": "0.00",
        "loanCreditLimit": "0.00",
        "loanBalance": "0.00",
        "projectedDdAmount": "0.00",
        "actualDirectDebitPaymentAmount": "0.00",
        "highBalanceAmount": "122.56",
        "lastPurchaseAmount": "120.00",
        "lastCashAdvancedAmount": "0.00",
        "loanAvailable": "0.00",
        "cashCreditLimit": "0.00",
        "creditLimit": "1,000.00",
        "currentDueAmount": "25.00",
        "pastDueAmount": "25.00",
        "incomeAmount": "0.00",
        "lastPaymentAmount": "0.00"
    },
    "chargeOffDetails": {
        "resetChargeoffDaysSwitch": "0",
        "additionalChargeOffReason": "",
        "chargeOffReason": "",
        "chargeOffStatus": "1",
        "chargeOffDaysCount": 0
    },
    "disputedDetails": {
        "disputedItemsCount": 0,
        "totalCashDisputedItemsAmount": "0.00",
        "cashDisputedAmount": "0.00",
        "cashDisputedItemsCount": 0
    },
    "pctOverrideDetails": {
        "pctOverride": "",
        "pctStartDate": "00/00/0000",
        "pctExpiryDate": "00/00/0000"
    },
    "accountId": "0004316830510010641",
    "businessUnit": 700,
    "customerId": "0004316830510010641",
    "status": "A",
    "billingCycle": 18,
    "isRestructureEnabled": "N",
    "numberOfUnblockedCards": 1,
    "relationshipId": "",
    "billingLevel": "1",
    "isVipEnabled": "0",
    "liabilityIndicator": "0",
    "employeeCode": "",
    "sourceCode": "MOBBANKIN1",
    "statementDeliveryMode": "P",
    "shortName": "NAME",
    "userAccountId": "0000000000000000000",
    "returnMailCount": 0,
    "returnMailUser": "",
    "returnMailDate": "00/00/0000",
    "permanentCollector": "",
    "correspondenceCustomerId": "",
    "letterRequest": "",
    "isFraudulentReportEnabled": "Y",
    "deferMembershipFeeDate": "00/00/0000",
    "residenceId": "B01",
    "issuanceId": "B01",
    "currencyCode": "36",
    "primaryAccountFlag": "",
	"productId": 1,
    "externalContractId": "",
    "addressId": "RESIDENTIAL",
    "billingAcctInd": "0"
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