# Board Account

This API is used to board the new account. API internally generate a new account number that identify record you are adding.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces

## Endpoint

`POST /v1/accounts/boardAccount`

## Payload Example

### Request Payload

```json
{
  "expirationDateOfPctOverride": 0,
  "primaryAccountFlag": " ",
  "businessUnit": 600,
  "alternateCustomerNumber": " ",
  "expiryDateOfTempCreditLimit": 0,
  "cashPlanNumber": 0,
  "processingControlLevel": " ",
  "expireDateOfTheOverride": 0,
  "authorizationCriteriaTable": " ",
  "billingCurrency": 0,
  "ibsSavingsRoutingNumber": 12345,
  "ibsSavingsAccountNumber": 12345,
  "issuanceId": 600,
  "addInsuranceProduct": "N",
  "creditLimit": 15000,
  "billingLevel": 1,
  "suppressTknAtAccntLevel": 0,
  "product": 600,
  "corporateIdNumber": 0,
  "idOfThePctOverrideTables": " ",
  "owningBranchNumber": 999999998,
  "dualBillingFlag": 0,
  "retailPlanNumber": 0,
  "cardTechnology": 0,
  "customerNumber": 1000000007,
  "ibsDdaRoutingNumber": 0,
  "startDateOfPctOverride": 0,
  "residenceId": 600,
  "ibsDdaAccountNumber": " ",
  "startDateOfTheOverride": 0,
  "suppressLetter": 0,
  "waiveMembershipFees": 0,
  "billingCycle": 18,
  "coreBankingIndicator": "B",
  "cardNumberingScheme": 0,
  "relationshipLevelBillingCycle": 0,
  "customerSelectedDueDay": 0,
  "mobilePiFlag": 0,
  "shortName": "ABCDE",
  "temporaryCreditLimit": 0
}
``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/boardAccount).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `addInsuranceProduct` | Payload | *string* | 01 | This is the code that indicates whether to add an Insurance Product record. |
| `businessUnit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `customerNumber` | Payload | *string* | 19 | This is the code that indicates customer number. |
| `creditLimit` | Payload | *string* | 17 | This is the credit limit of the account. |
| `suppressLetter`| Payload | *number* | 01 | Code that indicates whether to suppress all letters for the account. |
| `billingCycle` | Payload | *number* | 02 | This flag indicates the day of the month that CMS performs cycle processing for the account. |
| `SupressToken` | Payload | *number* | 01 | Code that indicates whether the account is eligible for tokenization. |
| `coreBankingIndicator` | Payload | *string* | 01 | Code that indicates type of account. |
| `waiveMembershipFees` | Payload | *number* | 01 | Flag that indicates whether to waive the annual membership fee for the account. |
| `owningBranchNumber` | Payload | *number* | 09 | This field is the number of the branch that owns this account and location of financial reporting for this account. |
| `Product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |

### Successful Response Payload

```json
{
  "product": 1,
  "businessUnit": 600,
  "accountNumber": 0006000011000002430
}
```

### Error Response Payload

```json
{
   "errorCode" :  "V5SB4003EA" ,
   "errorMessage" : "Base account number is required"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5SB4003EA` | Base account number is required |
| `V5SB4003EG` | Base account number must be numeric |
| `V5SB4003EH` | Base account number required |
| `V5SB4005EA` | Customer NA account must be blank |
| `V5SB4005EB` | Customer NA account required |
| `V5SB4005EG` | Customer NA account must be blank |
| `V5SB4005EH` | Customer NA account must be numeric |
| `V5SB4008EA` | Relationship not valid for this Org |
| `V5SB4008EB` | Relationship not valid for the dual Org |
| `V5SB4001EA` | Org not on file |
| `V5SB4001SA` | Org not on file |
| `V5SB4002EA` | Logo record not on file |
| `V5SB4002EB` | Logo record is incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid account |
| `V5SB4012EA` | Sweeping not allowed in this logo |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |
| `V5SB4012EC` | Account type must be zero for prepaid account |
| `V5SB4157EC` | Account number exist on relationship file for this org |
| `V5SB4157ED` | Account number exist on relationship file for dual org |
| `V5SB4158EA` | Account number cannot duplicate existing embosser for this org |
| `V5SB4158EB` | Account number cannot duplicate existing embosser for dual org |
| `V5SB4151EA` | Logo does not allow billing account generation |
| `V5SB4151EB` | Maximum nummber 20 attemptds made on billing account |
| `V5SB4151EC` | Generated account number IS greater than ending billing number|
| `V5SB4151ED` | Logo does not allow account number generation |
| `V5SB4151EE` | Maximum nummber 20 attemptds made on Base account number |
| `V5SB4151EG` | Generated account number IS greater than Base account number|
| `V5SB4152EB` | Org does not allow account number generation |
| `V5SB4160EA` | Invalid Base account number digit for this org |
| `V5SB4160EB` | Invalid Base account number for this Org |
| `V5SB4160EC` | Invalid Base account number digit for dual org |
| `V5SB4160ED` | Invalid Base account number for dual org |