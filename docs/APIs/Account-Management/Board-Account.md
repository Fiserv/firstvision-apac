# Board Account

This API is used to board the new account. It can be invoked with required details and new account number will be created in real time.
Fields that are not provided in the Request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

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
| `Base Account Number` | Payload | *string* | 19 | This is the identification number to assign to the new Account Base Segment record. |
| `Create Account Record` | Payload | *string* | 1 | This is the code that indicates whether to add a new account record. |
| `Business Unit` | Payload | *number* | 3 | Identification number of the business unit associated with the  account or relationship. |
| `Product` | Payload | *number* | 3 | Identification number of the product associated with the  account or relationship. |
| `Customer Number` | Payload | *string* | 19 | This is the code that indicates customer number. |
| `Credit Limit` | Payload | *string* | 17 | This is the Credit limit of the account. |
| `Billing Cycle` | Payload | *number* | 02 | This flag indicates the day of the month that CMS performs cycle processing for the account. |

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
   "errorMessage" : "Base Account number is required"   
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
| `V5SB4008EA` | Relationship not valid for this ORG |
| `V5SB4008EB` | Relationship not valid for the dual ORG |
| `V5SB4001EA` | Organization not on file |
| `V5SB4001SA` | Organization not on file |
| `V5SB4002EA` | LOGO record not on file |
| `V5SB4002EB` | LOGO record is incomplete |
| `V5SB4009EA` | Relationship number required |
| `V5SB4011EA` | Insurance not allowed for prepaid account |
| `V5SB4012EA` | Sweeping not allowed in this LOGO |
| `V5SB4012EB` | HCS must be active for account type values 1,2,3 |
| `V5SB4012EC` | Account type must be zero for prepaid account |
| `V5SB4157EC` | Account number exist on relationship file for this ORG |
| `V5SB4157ED` | Account number exist on relationship file for DUAL ORG |
| `V5SB4158EA` | Account number cannot duplicate existing embosser for this ORG |
| `V5SB4158EB` | Account number cannot duplicate existing embosser for DUAL ORG |
| `V5SB4151EA` | LOGO does not allow billing account generation |
| `V5SB4151EB` | Maximum nummber 20 attemptds made on billing account |
| `V5SB4151EC` | Generated account number IS greater than ending billing number|
| `V5SB4151ED` | LOGO does not allow account number generation |
| `V5SB4151EE` | Maximum nummber 20 attemptds made on Base account number |
| `V5SB4151EG` | Generated account number IS greater than Base account number|
| `V5SB4152EB` | ORG does not allow account number generation |
| `V5SB4160EA` | Invalid Base account number digit for this ORG |
| `V5SB4160EB` | Invalid Base account number for this Org |
| `V5SB4160EC` | Invalid Base account number digit for DUAL ORG |
| `V5SB4160ED` | Invalid Base account number for DUAL ORG|