# Release 24.11-Minor - Version 1.12.0

## Date: 21/11/2024

### General Changes

- NA

#### Documentation Change in Swagger

- Inquire Account: New fields creditLimitLastDecreasedDate, creditLimitLastIncreasedDate under dateFieldsDetails, new fields maximumEligibleBalanceForTransactionInstalment, eligibleBalanceForStatementInstalment and updatedQualificationGraceBalance,membershipFeeRefundAmount, cardFeeRebateAmount under amountDetails and new group productTrasfer (businessUnit, productId, accountId, effetciveDate) added in response.
- Inquire Account Plan: New field cycleToDateEligiblePurchaseAmountForTransactionInstalment added in response.
- Inquire Plan Controls: New values 4 added to typeofLoan existing field, new fields isWaiveProrataEnabled under loanCancellationControls and transactionInstalmentConversionEligibilityIndicator under instalmentControls added in response.
- Inquire Loan: New values 4 added to typeofLoan, value 7 added to closeReason existing field, new field activationDate under loanDisclosedAndInitialAmountDetails added in response.
- List Loans by Account - New values 4 added to typeofLoan, value 7 added to closeReason existing field in response
- List Billed Transactions: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- List Unbilled Transactions: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- List Outstanding Authorizations: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- Inquire Statement Transaction Details: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- List Transactions by Date Range: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- List Transactions by Date Range V2: New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response.
- List Statment Eligible Plan Balance: New fields accountEligibleBalanceForStatementInstalment and todayConvertedStatementInstalmentBalance added in response. 
- Statement Balance Conversion: planDetails1-5 deleted from request and statementInstalmentRequestedAmount added in request. Also statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response 
- Statement Balance Simulation: planDetails1-5 deleted from request and statementInstalmentRequestedAmount added in request. Also statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response
- Inquire Card: New field fraudTransferAccountId added in response
- Product Transfer: Existing field transferToAccountId is deleted and defaulted with '/' and updated existing field transferToProdcutId as mandatory.

### New APIs

#### Inquire Maximum Eligible Transaction Amount

This API will be called to get the maximum eligible transaction amount for TIP loans for a given Account and Promo Plan provided in the input.

#### Unsettled Transaction Conversion

This API supports conversion unsettled transactions into instalments for a given accountId/paymentInstrumentId and other details. API first validates if given transactions are eligible to convert into instalment. If transactions are eligible, then system converts given transactions into instalment.

#### Unsettled Transaction Simulation

This API supports conversion unsettled transactions into instalments for a given accountId/paymentInstrumentId and other details. API first validates if given transactions are eligible to convert into instalment. If eligible then system responds with loan scheduling details.

#### Inquire Account Payoff Quote  

This API is used to fetch calculated payoff amount details for a given accountId.

#### Reverse Product Transfer

This API is used to reverse transfer of the account and all the cards associated to it to a old product.

#### Pay All

This API is used process pay all transactions for a given payment instrument Id or payment card number.

### Updated APIs -

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | Inquire Account | •  New field creditLimitLastDecreasedDate, creditLimitLastIncreasedDate,maximumEligibleBalanceForTransactionInstalment, eligibleBalanceForStatementInstalment and updatedQualificationGraceBalance, membershipFeeRefundAmount, cardFeeRebateAmount added in response |
| 2 | Account Management | List Billed Transactions | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 3 | Account Management | List Outstanding Authorizations | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 4 | Account Management | List Unbilled Transactions | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 5 | Account Management | Inquire Statement Transaction Details | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 6 | Account Management | List Transactions by Date Range | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 7 | Account Management | List Transactions by Date Range V2 | • New fields transactionIdentifier, recurringTransactionIndicator and multiClearingSequenceIndicator added in response |
| 8 | Account Management | Inquire Account plan | • New field cycleToDateEligiblePurchaseAmountForTransactionInstalment added in response |
| 9 | Account Management | Product Transfer | • Existing field transferToAccountId is deleted and defaulted with '/' and updated existing field transferToProdcutId as mandatory |
| 10 | Loans Management | Inquire Plan Controls | • New field isWaiveProrataEnabled added in response •  New values 4 added to typeofLoan existing field |
| 11 | Loans Management | Inquire Loan | • New field activationDate added in response •  New values 4 added to typeofLoan and 7 to closeReason |
| 12| Loans Management | List Loans by Account | • New field activationDate added in response •  New values 4 added to typeofLoan and 7 to closeReason |
| 13 | Loans Management | Statement Balance Simulation | • planDetails1-5 deleted from request •  statementInstalmentRequestedAmount added in request •  statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response. |
| 14 | Loans Management | Statement Balance Conversion | • planDetails1-5 deleted from request •  statementInstalmentRequestedAmount added in request •  statementInstalmentRequestedAmount, statementInstalmentConvertedAmount, qualificationGraceBalance added in response. |
| 15 | Loan Management | List Statment Eligible Plan Balance | • New fields accountEligibleBalanceForStatementInstalment and todayConvertedStatementInstalmentBalance added in response |
| 16 | Card Management | Inquire Card | • New field fraudTransferAccountId added in response |

### Deleted APIs

N/A
