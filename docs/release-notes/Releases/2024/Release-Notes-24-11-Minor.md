# Release 24.11-Minor - Version 1.12.0

## Date: 21/11/2024

### General Changes

- NA

#### Documentation Change in Swagger

- Inquire Account: New fields creditLimitLastDecreasedDate, creditLimitLastIncreasedDate under dateFieldsDetails, new fields maximumEligibleBalanceForTransactionInstalment, eligibleBalanceForStatementInstalment and updatedQualificationGraceBalance under amountDetails added in response.
- Inquire Account Plan: New field cycleToDateEligiblePurchaseAmountForTransactionInstalment added in response.
- Inquire Plan Controls: New values 4 added to typeofLoan existing field, new fields isWaiveProrataEnabled under loanCancellationControls and transactionInstalmentConversionEligibilityIndicator under instalmentControls added in response.
- Inquire Loan: New values 4 added to typeofLoan, value 7 added to closeReason existing field, new field activationDate under loanDisclosedAndInitialAmountDetails added in response.
- List Loans by Account - ew values 4 added to typeofLoan, value 7 added to closeReason existing field in response
- List Billed Transactions: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- List Unbilled Transactions: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- List Outstanding Authorizations: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- Inquire Statement Transaction Details: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- List Transactions by Date Range: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- List Transactions by Date Range V2: New fields transactionIdentifier and multiClearSequenceIndicator added in response.
- List Statment Eligible Plan Balance: New fields accountEligibleBalanceForStatementInstalment and todayConvertedStatementInstalmentBalance added in response. 
- Statement Balance Conversion: planDetails1-5 deleted from request and statementInstalmentRequestedAmount added in request. Also statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response 
- Statement Balance Simulation: planDetails1-5 deleted from request and statementInstalmentRequestedAmount added in request. Also statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response

### New APIs

#### Inquire Maximum Eligible Transaction Amount

This API will be called to get the maximum eligible transaction amount for TIP loans for a given Account and Promo Plan provided in the input.

#### Unsettled Transaction Conversion

This API supports conversion unsettled transactions into instalments for a given accountId/paymentInstrumentId and other details. API first validates if given transactions are eligible to convert into instalment. If transactions are eligible, then system converts given transactions into instalment.

#### Unsettled Transaction Simulation

This API supports conversion unsettled transactions into instalments for a given accountId/paymentInstrumentId and other details. API first validates if given transactions are eligible to convert into instalment. If eligible then system responds with loan scheduling details.

#### Inquire Account Payoff Quote  

This API is used to fetch calculated payoff amount details for a given accountId.

### Updated APIs -

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | Inquire Account | <ul> <li> New field creditLimitLastDecreasedDate, creditLimitLastIncreasedDate,maximumEligibleBalanceForTransactionInstalment, eligibleBalanceForStatementInstalment and updatedQualificationGraceBalance added in response |
| 2 | Account Management | List Billed Transactions | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 3 | Account Management | List Outstanding Authorizations | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 4 | Account Management | List Unbilled Transactions | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 5 | Account Management | Inquire Statement Transaction Details | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 6 | Account Management | List Transactions by Date Range | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 7 | Account Management | List Transactions by Date Range V2 | <ul> <li> New fields transactionIdentifier and multiClearSequenceIndicator added in response |
| 8 | Account Management | Inquire Account plan | <ul> <li> New field cycleToDateEligiblePurchaseAmountForTransactionInstalment added in response |
| 9 | Loans Management | Inquire Plan Controls | <ul> <li> New field isWaiveProrataEnabled added in response. </li> <li> New values 4 added to typeofLoan existing field |
| 10 | Loans Management | Inquire Loan | <ul> <li> New field activationDate added in response. </li> <li> New values 4 added to typeofLoan and 7 to closeReason |
| 11| Loans Management | List Loans by Account | <ul> <li> New field activationDate added in response. </li> <li> New values 4 added to typeofLoan and 7 to closeReason |
| 12  Loans Management | Statement Balance Simulation | <ul> <li> planDetails1-5 deleted from request. </li> <li> statementInstalmentRequestedAmount added in request. </li> <li> statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response. |
| 13 | Loans Management | Statement Balance Conversion | <ul> <li> planDetails1-5 deleted from request. </li> <li> statementInstalmentRequestedAmount added in request. </li> <li> statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response. |
| 14 | Loan Management | List Statment Eligible Plan Balance | <ul> <li> New fields accountEligibleBalanceForStatementInstalment and todayConvertedStatementInstalmentBalance added in response |

### Deleted APIs

N/A
