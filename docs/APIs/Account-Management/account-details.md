# Inquire Account Details

The service provides the basic details of the account associated with the customer. This API can be called using business unit and account number.

## Endpoint

`GET /v1/accounts/{accountNumber}/details`

## Payload Example

### Request Payload

```json

Shoud be empty.
***The Business Unit and Account Number should be sent as query parameters and path variable.*** 

```   

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |

### Successful Response Payload

```json
{
  "businessUnit": 200,
  "userDefinedChargeOffReason": " ",
  "cardScheme": 3,
  "alternateCustomerNumber": 0,
  "collateralCode": " ",
  "customerStatementFlag": 1,
  "customerStatementLetterFlag": 1,
  "correspondenceCustomerNumber": " ",
  "cardFeeDate": "00/00/0000",
  "flexBillingFlag": "N",
  "permanentCollector": " ",
  "returnMailDate": "00/00/0000",
  "creditLimit": "$0.00",
  "chargeOffStatus": 0,
  "letterRequest": " ",
  "userAccountNumber": 0,
  "returnMailUser": " ",
  "internalStatus": "D",
  "altCustomerExpiryDate": "00/00/0000",
  "nextStatementDate": "31/08/2021",
  "dateLastMaintenance": "2021-09-11",
  "billingCycle": 31,
  "reissueScheme": 0,
  "accountDisplayRequest": "N",
  "dateAccountOpened": "17/08/2021",
  "ownerFlag": " ",
  "statementReprintDate": "00/00/0000",
  "vipStatus": 0,
  "shortName": "TESTING",
  "applicationDate": "00/00/0000",
  "primaryAccountFlag": " ",
  "statementFlag": " ",
  "incomeOfTheAccount": "$0.00",
  "numberOfUnblockedCards": 2,
  "restructureFlag": "N",
  "altCustomerAddressEffectiveDate": "00/00/0000",
  "statementFrequency": 1,
  "reportFraudulentActivity": "N",
  "dueDay": 0,
  "dateClosed": "00/00/0000",
  "employeeCode": " ",
  "blockCodeDate1": "00/00/0000",
  "dateNextCrIntPymt": "00/00/0000",
  "blockCodeDate2": "00/00/0000",
  "returnMailCounter": 0,
  "ccmCustomerId": " ",
  "numberOfChargeOffDays": 0,
  "billingLevel": 1,
  "highBalanceAmount": "$0.00",
  "dateLastCycle": "31/07/2021",
  "product": 1,
  "deferMembershipFeeDate": "00/00/0000",
  "dualBillingFlag": 0,
  "systemDefinedChargeOffReason": " ",
  "memoBillingCurrency": 36,
  "resetChargeoffDaysSwitch": 0,
  "alternateCustomerNumberFlag": " ",
  "customerNumber": 2000002000007799,
  "accountNumber": 70369818052278,
  "liabilityIndicator": 0,
  "collateralCardRequest": "N",
  "billingAcctInd": 0,
  "dateOfNotificationReceived": "00/00/0000",
  "relationshipNumber": " ",
  "statementReprintFlag": "C",
  "greatestExpiryDate": "16/08/2024",
  "blockCode1": " ",
  "cardExpirationDate": "00/00/0000",
  "blockCode2": " ",
  "currencyCode": 36
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0004SF",
  "errorMessage": "Get Request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get Request - Record not found|
