# Release 23.02-Minor - Version 1.1.0

## Date: 16/02/2023

### General Changes

#### Additional Header fields in APIs

In preparation of passing API tracking details, following additional headers are added in each API. These headers are optional and currently not fully functional from Vision side.  The full functionality will be rolled out in subsequent releases.
x-client-correlation-id
x-client-trace-id
x-client-source-channel
x-client-user-id

#### Documentation Change in Swagger

- Description change for businessUnit from 001-998 to 1-998 and recordNumber from 000 to 0.as these fields are integer
- Optimization and correct maxLength for amount and rate fields in all APIs
- 422 error message is added in list of response code in API Explorer for all APIs

### New APIs

#### Reverse Authorization

This API is used to reverse the authorization for a given payment instrument Id or payment card number, authorization code, effective date, and transaction amount, if given.
Reverse is possible for any authorization which is waiting for settlement.

#### Inquire Loan

This API is used to fetch Loan details like Loan disclosed and initial amount of loan, loan disbursement details, loan top-up redraw can restructure detail, fixed interest and skip payment details for a given account Id.

#### Inquire Loan Schedule

This API is used to fetch loan schedule details for the current loan data.

#### Inquire Original Loan

This API is used to fetch existing loan plan records. It contains the original precomputed amounts and other original information received for a loan plan for a given account Id.

#### Loan Calculator

This API is used to calculate the loan repayment options for prospective borrowers based on the details given input request.

### Updated APIs

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | List Outstanding Authorizations | <ul> <li> Added remainingAuthorizationAmount in response |
| 2 | Account Management | List Unbilled Transactions | <ul> <li> Added remainingAuthorizationAmount in response |
| 3 | Account Management | List Billed Transactions | <ul> <li> Removed pagination fields from response <li> Added pagination fields in response-header |
| 4 | Account Management | Inquire Statement Transaction Details | <ul> <li> Added below fields in response <ul> <li> addOnAmount </li> <li> overLimitAmount </li>  </ul> <li> Removed billingCurrency from response </li> <li> Removed pagination fields from response </li> <li> Added pagination fields in response-header </li>|
| 5 | Account Management | List Transactions by Date Range | <ul> <li> Added below fields in response <ul> <li> remainingAuthorizationAmount </li> <li> authorizationCode </li> </ul> <li> Description change for existing field transactionIndicator |
| 6 | Account Management | Inquire Account | <ul> <li> Added productId in response </li> <li> Label name change for below field in response <ul> <li> cashDisputedAmout to cahsDisputedAmount |
| 7 | Account Management | Board Account | <ul> <li> Removed billingCurrency from response |
| 8 | Miscellaneous | Board Entities | <ul> <li> Removed billingCurrency from response |
| 9 | Authorization | Request Authorization | <ul> <li> Added openToBuy in response |
| 10 | Authorization | Inquire Authorization | <ul> <li> Restructured the request message for better user experience |
| 11 | Customer Management | List Customers' Cards and Accounts | <ul> <li> Label name change for below fields in response <ul> <li>  numberOfTokens to tokenCount </li> <li> noOfTokenizedCards to totalTokenizedCardCount |
| 12 | Customer Management | List Customers' Cards | <ul> <li> Label name change for below field in response <ul> <li> numberOfTokens to tokenCount |
| 13 | Customer Management | List Customers' Accounts | <ul> <li> Label name change for below field in response <ul> <li> noOfTokenizedCards to totalTokenizedCardCount |
| 14 | Account Management | List Plans | <ul> <li> Label name change for below field in response <ul> <li> principalBalance to principalAmount |
| 15 | Miscellaneous | Inquire Business Unit | <ul> <li> Label name changes for below fields in response <ul> <li> dateNextProcess to nextProcessingDate </li> <li> dateLastMaintenance to  lastMaintenanceDate </li> <li> dateInterestAccruedThrough to interestAccruedThroughDate |

### Deleted APIs

N/A
