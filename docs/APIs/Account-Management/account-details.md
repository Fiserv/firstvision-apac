# Inquire Account Details

The service provides the basic details of the account associated with the customer. Some basic details include short name, credit limit, billing cycle etc.

## Endpoint

`GET /v1/accounts/{accountNumber}/details`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |

### Successful Response Payload

```json
{
  "businessUnit": 200,
  "accountNumber": "0002000010000403266",
  "product": 1,
  "billingAcctInd": 0,
  "shortName": "TESTING",
  "customerNumber": "0002000002000007799",
  "alternateCustomerNumberFlag": "",
  "alternateCustomerNumber": "0000000000000000000",
  "userAccountNumber": "0000000000000000000",
  "internalStatus": "D",
  "chargeOffStatus": "0",
  "blockCode1": "",
  "blockCode2": "",
  "billingCycle": 31,
  "statementFlag": "",
  "statementFrequency": "1",
  "returnMailCounter": 0,
  "returnMailUser": "",
  "returnMailDate": "00/00/0000",
  "permanentCollector": "",
  "collateralCode": "",
  "ownerFlag": "",
  "employeeCode": "",
  "letterRequest": "",
  "collateralCardRequest": "N",
  "accountDisplayRequest": "N",
  "restructureFlag": "N",
  "statementReprintFlag": "C",
  "flexBillingFlag": "N",
  "applicationDate": "00/00/0000",
  "dateAccountOpened": "17/08/2021",
  "blockCodeDate1": "00/00/0000",
  "blockCodeDate2": "00/00/0000",
  "dateClosed": "00/00/0000",
  "cardFeeDate": "00/00/0000",
  "nextStatementDate": "31/08/2021",
  "dateLastMaintenance": "09/12/2021",
  "altCustomerExpiryDate": "00/00/0000",
  "statementReprintDate": "00/00/0000",
  "dateOfNotificationReceived": "00/00/0000",
  "cardExpirationDate": "00/00/0000",
  "creditLimit": "$0.00",
  "highBalanceAmount": "$0.00",
  "incomeOfTheAccount": "$0.00",
  "numberOfUnblockedCards": 2,
  "numberOfChargeOffDays": 0,
  "resetChargeoffDaysSwitch": "0",
  "reportFraudulentActivity": "N",
  "systemDefinedChargeOffReason": "",
  "userDefinedChargeOffReason": "",
  "greatestExpiryDate": "16/08/2024",
  "relationshipNumber": "",
  "cardScheme": "3",
  "primaryAccountFlag": "",
  "reissueScheme": "0",
  "dateLastCycle": "31/07/2021",
  "memoBillingCurrency": 36,
  "customerStatementFlag": "1",
  "customerStatementLetterFlag": "1",
  "currencyCode": 36,
  "billingLevel": "1",
  "vipStatus": "0",
  "dualBillingFlag": "0",
  "liabilityIndicator": "0",
  "dueDay": 0,
  "deferMembershipFeeDate": "00/00/0000",
  "correspondenceCustomerNumber": "",
  "altCustomerAddressEffectiveDate": "00/00/0000",
  "ccmCustomerId": "",
  "dateNextCrIntPymt": "00/00/0000"
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