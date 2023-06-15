# Release 23.08-Minor - Version 1.4.0

## Date: 24/08/2023

### General Changes

- Amount/Credit limit validation added in API transformation layer for below APIs
  - Monetary Action
  - Post Payments
  - Inquire Auth
  - Request Auth
  - Reverse Auth
  - Loan Calculator
  - Board Card
  - Update Product Card Controls		

#### Documentation Change in Swagger

- Board Card: Label name change from 'visaMiniCardVersion' to 'visaMiniIndicator'
- ApplePay Push Provisioning: nonce field is now mandatory in input request 
- Inquire Authorization Details: Label name change from ‘transactionAmount’ to ‘authorizationAmount’
- Change PIN: Label name change from 'pinSetOrResetActionCode' to 'pinChangeActionCode' and 'pinSetOrResetMemo' to 'pinChangeMemo'
- Inquire Account: Maximum length changed to 24 for cashCreditLimit, cashBalance, openToBuy, creditLimit, currentBalance, loanCreditLimit, loanAvailable, loanBalance and cashAvailable fields. 
  - Block code example updated with value from blank.
  - Example corrected for returnMailCount description.
- Inquire Card: Block code example updated with value from blank.
- Block Unblock Account: Block code/date example updated with value from blank.
- Block Unblock Card: Block code/date example updated with value from blank.
- Inquire Account Plan: Example corrected for rateTableOccurrenceIndicator description.
- Inquire Statement Plan Details: Example corrected for billingCycle description.
- Product Transfer: Example corrected for billingCycle description.
- Inquire Auth: Example corrected for collectionReason description.

### New APIs

#### Add iPlan

This API is used to create iPlan record for a given details in request.

#### Snooze iPlan

This API is used to snooze the iPlan.

#### Update Payment Occurrence

This API is used to update the payment occurrence.

#### Update Configuration Template

This API is used to update the configuration template.

#### Update Snooze Count

This API is used to update the snooze count for a given iPlan.

#### Reset Snooze Count

This API is used to reset the snooze count for a given iPlan.

#### Update BNPL Controls

This API is used to update the snooze count for a given iPlan.

#### Board Entities(version 2)

This API is used to add Customer Name/Address record, Account Base Segment record, Embosser record, and Relationship record and Insurance record based on the input criteria. This is new version 2 build for board entitiy API where label type is corrected from string to integer.

### Updated APIs

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | List Billed Transactions | <ul> <li>  Added below fields in response <ul> <li> merchantCountryCode <li> upiMerchantId   |
| 2 | Account Management | List Unbilled Transactions | <ul> <li> Added below fields in response <ul> <li> merchantCountryCode <li> upiMerchantId   |
| 3 | Account Management | List Outstanding Authorizations | <ul> <li> Added below fields in response <ul> <li> merchantCountryCode <li> upiMerchantId   |
| 3 | Account Management | Inquire Statement Transaction Details | <ul> <li> Added below fields in response <ul> <li> merchantCountryCode <li> upiMerchantId   |
| 4 | Account Management | Inquire Direct Debit Controls | <ul> <li> New value '8'(Qual Grace Balance) introduced for field nominatedType in response |
| 5 | Account Management | Update Direct Debit Controls | <ul> <li> New value '8'(Qual Grace Balance) introduced for field nominatedType in request and response |
| 6 | Account Management | Board Account | <ul> <li> Type changed from string to integer for below fields <ul> <li> billingLevel <li> dualBillingFlag <li> cardTechnology <li> isMobilePiEnabled <li> isSuppressLetterEnabled <li> isWaiveAnnualMembershipFeeEnabled <li> isSupressTokenEnabled | 
| 7 | Account Management | Inquire Account Preference | <ul> <li> Type changed from string to integer for below fields <ul> <li> ownerCoOwnerStatementFlag |
| 8 | Account Management | Inquire Payment History | <ul> <li> Type changed from string to integer for below fields <ul> <li> cycleDue |
| 9 | Account Management | Inquire Delinquency | <ul> <li> Type changed from string to integer for below fields <ul> <li> currentCycleDue |
| 10 | Account Management | Inquire Direct Debit Controls | <ul> <li> Type changed from string to integer for below fields <ul> <li> paymentRemittanceMethod <li> nominatedType <li> paymentType |
| 11 | Account Management | Inquire Payment History | <ul> <li> Type changed from string to integer for below fields <ul> <li> cycleDue <li> reversalIndicator |
| 12 | Account Management | Monetary Action | <ul> <li> Type changed from string to integer for below fields <ul> <li> actionCodePriority |
| 13 | Account Management | Product Transfer | <ul> <li> Type changed from string to integer for below fields <ul> <li> transferReplcementIndicator <li> continuewithReissue |
| 14 | Account Management | Update Acct Preference | <ul> <li> Type changed from string to integer for below fields <ul> <li> isSupressTokenEnabled |
| 15 | Account Management | Update Direct Debit | <ul> <li> Type changed from string to integer for below fields <ul> <li> paymentRemittanceMethod <li> nominatedType <li> paymentType|
| 16 | Account Management | Update Statement Preference | <ul> <li> Type changed from string to integer for below fields <ul> <li> ownerCoOwnerStatementFlag |
| 17 | Account Management | Update Token Supress Ind | <ul> <li> Type changed from string to integer for below fields <ul> <li> isSupressTokenEnabled |
| 18 | Account Management | Update Waive Fee  | <ul> <li> Type changed from string to integer for below fields <ul> <li> isWaiveLateChargeEnabled <li> isWaiveInterestFeeEnabled <li> isWaiveAnnualMembershipFeeEnabled <li> isWaiveOverlimitFeeEnabled <li> isWaiveNsf1-5FeeEnabled <li> isWaiveCardIssuanceFeeEnabled <li> isWaiveLetterFeeEnabled <li> isWaiveAddOnMembershipFeeEnabled <li> isWaiveTaxEnabled <li> isWaiveCycleSpendFeeEnabled <li> UserFees (6 fields) <li> CashAdvanceFees (6fields) <li> ServiceFees (25fields) |
| 19 | BNPL | Inquire Offer Codes | <ul> <li> Type changed from string to integer for below fields <ul> <li> bnplType |
| 20 | Loan Management | Inquire Loan | <ul> <li> Type changed from string to integer for below fields <ul> <li> isInterestCapIndicatorEnabled <li> isInsuranceCapIndicatorEnabled <li> isUserFee * CapIndicatorEnabled <li> interestIndicator <li> insuranceIndicator <li> userFee * Indicator <li> accountIndicator <li> restructureReason <li> cancelExpiryDate  (Length/Description change) <li> nextInterestEffectiveDate (Description change) <li> interestIndicator <li> skipPaymentIndicator |
| 21 | Loan Management | Inquire Original loan | <ul> <li> Type changed from string to integer for below fields <ul> <li> initialInterestRebateIndicator <li> initialInsuranceRebateIndicator <li> initialUserFee * RebateIndicator <li> secondInterestRebateIndicator <li> secondInsuranceRebateIndicator <li> secondUserFee * RebateIndicator <li> rebatePeriodIndicator |
| 22 | Loan Management | Inquire Original loan | <ul> <li> Type changed from string to integer for below fields <ul> <li> isPaymentScheduledEnabled <li> interestMethod <li> roundingIndicator |
| 23 | User Management | Add User | <ul> <li> Type changed from string to integer for below fields <ul> <li> sourceGroupType |
| 24 | Authorization | Inquire Authorization Details | <ul> <li> Type changed from integer to string in response for chargeOffStatus |
| 25 | Card Management | Change PIN | <ul> <li> Deleted below fields in response <ul> <li> pinTryCounterResetActionCode </li> <li> pinTryCounterResetMemo |
| 26 | Card Management | Board Card | <ul> <li> Type changed from string to integer for below fields <ul> <li> cardAction </li> <li> name1TypeIndicator <li> cardholderFlag <li> visaMiniIndicator <li> mobileProvisionStatus |
| 27 | Card Management | Inquire Card | <ul> <li> Type changed from string to integer for below fields <ul> <li> cardAction <li> isSecureCodeEnabled <li> visaPlusIndicator <li> cardholderType <li> visaMiniCardVersion <li> isPinSuppressionEnabled <li> name1TypeIndicatoru <li> name2TypeIndicator <li> customersGender <li> mobileProvisionStatus  |
| 28 | Card Management | Inquire Card Preference | <ul> <li> Type changed from string to integer for below fields <ul> <li> issueDeliveryOption <li> reissueDeliveryOption |
| 29 | Card Management | Update Card Preference | <ul> <li> Type changed from string to integer for below fields <ul> <li> cardholderType <li> issueDeliveryOption <li> reissueDeliveryOption |
| 30 | Card Management | Update Card Type | <ul> <li> Type changed from string to integer for below fields <ul> <li> cardholderType |
| 31 | Card Management | Update Issue Reissue Delivery Option | <ul> <li> Type changed from string to integer for below fields <ul> <li> issueDeliveryOption <li> reissueDeliveryOption |
| 32 | Customer Management | Board Customer | <ul> <li> Type changed from string to integer for below fields <ul> <li> dualFlag <li> nameTypeIndicator * <li> residentialFlag <li> gender <li> emailAddressFlag |
| 33 | Customer Management | List Customers' Cards | <ul> <li> Type changed from string to integer for below fields <ul> <li> gender <li> cardHolderType <li> currentCardAction <li> lastCardAction <li> cardTechnology <li> isEcomEnabled |
| 34 | Customer Management | List Customers' Cards And Accounts | <ul> <li> Type changed from string to integer for below fields <ul> <li> gender |
| 35 | Customer Management | Update Customer | <ul> <li> Type changed from string to integer for below fields <ul> <li> homePhoneFlag <li> faxPhoneFlag <li> smsFlag <li> mobilePhoneFlag <li> phoneFlag  |
| 36 | Miscellaneous | Inquire Business Unit| <ul> <li> Type changed from string to integer for below fields <ul> <li> transactionBasedOffers <li> allowConsolidatedPayments <li> autoChargebackActive <li> actionOnLateFee <li> actionOnFinanceCharge <li> commercialCardsAllowed <li> excludeDefaultDisputedAmounts <li> earlySettlementQuotesProcess <li> installmentLoansActive |
| 37 | Product Management | Inquire Service Charge Table | <ul> <li> Added new bnplDetails group in request for BNPL functionality <li> Type changed from string to integer for below fields <ul> <li> transactionLimitFrequency </li> <li> method </li> <li> feePostingFrequency </li> <li> feePlan </li> <li> maximumIndicator |
| 38 | Product Management | Inquire Plan Master | <ul> <li> Type changed from string to integer for below fields <ul> <li> graceBalanceQualification <li> delinquencyLevelToCancel <li> cancellationPlanRollOverMethod <li> expirationRollover <li> expirationPlanRollOverMethod  |
| 39 | Product Management | Update Product Card Controls | <ul> <li> Type changed from string to integer for below fields <ul> <li> maximumAuthorizationLimitFrequency <li> isCountryRiskSpendLimitEnabled |
| 40 | Product Management | Inquire Product | <ul> <li> Type changed from string to integer for below fields <ul> <li> cardProductDisplay <li> isLoanFeatureEnabled  <li> isSameDayEmbossingEnabled <li> isChipOrPinCardEnabled<li> authAlerts <li> isSecureCodeEnabled <li> isDebitCardProcessEnabled<li> isTokenizationServiceEnabled <li> isManualPinResetEnabled<li> isCardActionTableEnabled <li> defaultCardTechnology<li> isScriptingEnabled <li> isSweepOptionEnabled<li> isCrossBorderAlertEnabled <li> creditLimitBypass<li> isLocalorInternationalUsageEnabled <li> NewCardDefaultEnabled<li> enhancedProductsEligible<li> pinMailerNameaddress<li> cardMailerNameaddress<li> isCardBureauFeedbackEnabled<li> pinOption<li>isOverlimitProcessingOptionIndicatorEnabled<li> openToBuyCreditBalance <li> includeDisputedAmounts<li> isWspTokenEnabled<li> prepaymentsAllowed |
| 41 | Product Management | Inquire Product | <ul> <li> Type changed from string to integer for below fields <ul> <li> interestRounding <li> examineCycleInterestVariance <li> allowNsfPaymentReversal <li> yearBase <li> tierLimitIndicator <li> rateIndexTable <li> isInterestOn * FeeEnabled <li> transactionQualification <li> isWaivePriorDeferredInterestEnabled <li> isPriorDeferredNsfPaymentReversalEnabled <li> priorDeferredInterestBalanceIndicator <li> isPriorDeferred * BalanceEnabled <li> priorDeferredPaidDateQualification <li> isWaiveCurrentCycleInterestEnabled <li> isCurrentCycleNsfPaymentReversalEnabled <li> currentCycleInterestBalanceIndicator <li> isCurrentCycle * BalanceEnabled <li> currentCyclePaidDateQualification <li> isWaivePriorCycleInterestEnabled <li> isPriorCycleNsfPaymentReversalEnabled <li> priorCycleInterestBalanceIndicator <li> isPriorCycle * BalanceEnabled <li> isWaiveResidualInterestEnabled <li> isResidualInterestNsfPaymentReversalEnabled <li> isResidualInterest * BalanceEnabled |

### Deleted APIs

N/A
