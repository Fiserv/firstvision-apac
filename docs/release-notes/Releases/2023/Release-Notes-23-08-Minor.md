# Release 23.08-Minor - Version 1.4.0

## Date: 24/08/2023

### General Changes

- Amount/Credit limit validation added in API transformation layer for below APIs
  - Monetary Action
  - Post Payments
  - Inquire Authorization Details
  - Request Authorization
  - Reverse Authorization
  - Loan Calculator
  - Board Card
  - Update Product Card Controls  

#### Documentation Change in Swagger

- Board Card: Label name change from visaMiniCardVersion to visaMiniIndicator
- ApplePay Push Provisioning: nonce field is now mandatory in input request
- Inquire Authorization Details: Label name change from transactionAmount to authorizationAmount
- Change PIN: Label name change from pinSetOrResetActionCode to pinChangeActionCode and pinSetOrResetMemo to pinChangeMemo
- Inquire Account:  API changes are mention in below points.
  - maxLength changed to 24 for cashCreditLimit, cashBalance, openToBuy, creditLimit, currentBalance, loanCreditLimit, loanAvailable, loanBalance and cashAvailable fields.
  - Example value updated from blank to 'X' in blockCode2.
  - Description updated for returnMailCount.
- Inquire Card: Example value updated from blank to 'X' in blockCode.
- Block Unblock Account: Example value updated from blank to 'X' in blockCode2.
- Inquire Account Plan: Description updated for rateTableOccurrenceIndicator.
- Inquire Statement Plan Details: Description updated for billingCycle.
- Product Transfer: Description updated for billingCycle.
- Inquire Authorization Details: Description updated for collectionReason.
- Inquire Loan:  Description change for cancelExpiryDate and nextInterestEffectiveDate. Also, maxLength change for cancelExpiryDate.
- Request Authorization: maxLength change for internalReferenceNumber
- Reverse Authorization: maxLength change for internalReferenceNumber
- List Transactions by Dare Range: Label change for merchantCountry to merchantCountryCode

### New APIs

#### Add iPlan

This API is used to create iPlan record for given details in account Id, instalment amount and other details.

#### Snooze iPlan

This API is used to snooze the iPlan for a given account Id.

#### Update Payment Occurrence

This API is used to update the payment occurrence for a given account's iPlan.

#### Update Configuration Template

This API is used to update the configuration template for a given account's iPlan.

#### Update Snooze Count

This API is used to update the snooze count for a given account's iPlan.

#### Reset Snooze Count

This API is used to reset the snooze count for a given account's iPlan.

#### Update BNPL Controls

This API is used to update BNPL controls at account level for a given account Id.

#### Board Entities V2 (version 2)

This API is used to add Customer Name/Address record, Account Base Segment record, Embosser record, and Relationship record and Insurance record based on the input criteria. This is new version 2 build for board entitiy API where label type is corrected from string to integer.

### Updated APIs

| S.No | Category             | API Name                               | Change                                                                                                        |
|------|----------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 1    | Account Management   | List Billed Transactions               | • Added below fields in response  • merchantCountryCode                                                                                       |
| 2    | Account Management   | List Unbilled Transactions             | • Added below fields in response  • merchantCountryCode                                                                                       |
| 3    | Account Management   | List Outstanding Authorizations        | • Added below fields in response  • merchantCountryCode                                                                                       |
| 3    | Account Management   | Inquire Statement Transaction Details  | • Removed currentBalance in response  • Added below fields in response  • merchantCountryCode                                                                                       |
| 4    | Account Management   | Inquire Direct Debit Controls          | • New value '8' (Qual Grace Balance) introduced for field nominatedType in response                           |
| 5    | Account Management   | Update Direct Debit Controls           | • New value '8' (Qual Grace Balance) introduced for field nominatedType in request and response               |
| 6    | Card Management      | Change PIN                             | • Deleted below fields in response  • pinTryCounterResetActionCode  • pinTryCounterResetMemo                                                                                    |
| 7    | Product Management   | Inquire Service Charge Table           | • Added new bnplDetails group in request for BNPL functionality  • Type changed from string to integer for below fields  • transactionLimitFrequency  • method  • feePostingFrequency  • feePlan  • maximumIndicator                                                                                          |
| 8    | Account Management   | Board Account                          | • ** Type changed from string to integer for below fields • billingLevel • dualBillingFlag • cardTechnology • isMobilePiEnabled • isSuppressLetterEnabled • isWaiveAnnualMembershipFeeEnabled • isSupressTokenEnabled  |
| 9    | Account Management   | Inquire Account Preference             | • Type changed from string to integer for below fields  • ownerCoOwnerStatementFlag                                                                                 |
| 10   | Account Management   | Inquire Payment History                | • Type changed from string to integer for below fields  • cycleDue                                                                                                  |
| 11   | Account Management   | Inquire Delinquency                    | • Type changed from string to integer for below fields  • currentCycleDue                                                                                           |
| 12   | Account Management   | Inquire Direct Debit Controls          | • Type changed from string to integer for below fields  • paymentRemittanceMethod  • nominatedType  • paymentType                                                                                               |
| 13   | Account Management   | Inquire Payment History                | • Type changed from string to integer for below fields  • cycleDue  • reversalIndicator                                                                                        |
| 14   | Account Management   | Monetary Action                        | • Type changed from string to integer for below fields  • actionCodePriority                                                                                       |
| 15   | Account Management   | Product Transfer                       | • Type changed from string to integer for below fields  • transferReplcementIndicator  • continuewithReissue                                                                                      |
| 16   | Account Management   | Update Acct Preference                 | • Type changed from string to integer for below fields  • isSupressTokenEnabled                                                                                    |
| 17   | Account Management   | Update Direct Debit                    | • Type changed from string to integer for below fields  • paymentRemittanceMethod  • nominatedType  • paymentType                                                                                               |
| 18   | Account Management   | Update Statement Preference            | • Type changed from string to integer for below fields  • ownerCoOwnerStatementFlag                                                                                |
| 19   | Account Management   | Update Token Supress Ind               | • Type changed from string to integer for below fields  • isSupressTokenEnabled                                                                                    |
| 20   | Account Management   | Update Waive Fee                       | • Type changed from string to integer for below fields  • isWaiveLateChargeEnabled  • isWaiveInterestFeeEnabled  • isWaiveAnnualMembershipFeeEnabled  • isWaiveOverlimitFeeEnabled  • isWaiveNsf1-5FeeEnabled  • isWaiveCardIssuanceFeeEnabled  • isWaiveLetterFeeEnabled  • isWaiveAddOnMembershipFeeEnabled  • isWaiveTaxEnabled  • isWaiveCycleSpendFeeEnabled  • UserFees (6 fields)  • CashAdvanceFees (6 fields)  • ServiceFees (25 fields)                                                                                   |
| 21   | BNPL                 | Inquire Offer Codes                    | • Type changed from string to integer for below fields  • bnplType                                                                                                  |
| 22   | Loan Management      | Inquire Loan                           | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • isInterestCapIndicatorEnabled                                                                            |
|      |                      |                                        |   • isInsuranceCapIndicatorEnabled                                                                           |
|      |                      |                                        |   • isUserFeeCapIndicatorEnabled                                                                             |
|      |                      |                                        |   • interestIndicator                                                                                        |
|      |                      |                                        |   • insuranceIndicator                                                                                       |
|      |                      |                                        |   • userFeeIndicator                                                                                         |
|      |                      |                                        |   • accountIndicator                                                                                        |
|      |                      |                                        |   • restructureReason                                                                                       |
|      |                      |                                        |   • skipPaymentIndicator                                                                                    |
| 23   | Loan Management      | Inquire Original loan                  | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • initialInterestRebateIndicator                                                                           |
|      |                      |                                        |   • initialInsuranceRebateIndicator                                                                          |
|      |                      |                                        |   • initialUserFeeRebateIndicator                                                                            |
|      |                      |                                        |   • secondInterestRebateIndicator                                                                            |
|      |                      |                                        |   • secondInsuranceRebateIndicator                                                                           |
|      |                      |                                        |   • secondUserFeeRebateIndicator                                                                             |
|      |                      |                                        |   • rebatePeriodIndicator                                                                                   |
| 24   | Loan Management      | Inquire Original loan                  | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • isPaymentScheduledEnabled                                                                                |
|      |                      |                                        |   • interestMethod                                                                                           |
|      |                      |                                        |   • roundingIndicator                                                                                        |
| 25   | User Management      | Add User                               | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • sourceGroupType                                                                                          |
| 26   | Authorization        | Inquire Authorization Details          | • Type changed from integer to string in response for chargeOffStatus                                        |
| 27   | Card Management      | Board Card                             | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cardAction                                                                                               |
|      |                      |                                        |   • name1TypeIndicator                                                                                       |
|      |                      |                                        |   • cardholderFlag                                                                                           |
|      |                      |                                        |   • visaMiniIndicator                                                                                        |
|      |                      |                                        |   • mobileProvisionStatus                                                                                    |
| 28   | Card Management      | Inquire Card                           | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cardAction                                                                                               |
|      |                      |                                        |   • isSecureCodeEnabled                                                                                       |
|      |                      |                                        |   • visaPlusIndicator                                                                                        |
|      |                      |                                        |   • cardholderType                                                                                           |
|      |                      |                                        |   • visaMiniCardVersion                                                                                      |
|      |                      |                                        |   • isPinSuppressionEnabled                                                                                  |
|      |                      |                                        |   • name1TypeIndicator                                                                                       |
|      |                      |                                        |   • name2TypeIndicator                                                                                       |
|      |                      |                                        |   • customersGender                                                                                          |
|      |                      |                                        |   • mobileProvisionStatus                                                                                    |
| 29   | Card Management      | Inquire Card Preference                | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • issueDeliveryOption                                                                                      |
|      |                      |                                        |   • reissueDeliveryOption                                                                                    |
| 30   | Card Management      | Update Card Preference                 | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cardholderType                                                                                           |
|      |                      |                                        |   • issueDeliveryOption                                                                                      |
|      |                      |                                        |   • reissueDeliveryOption                                                                                    |
| 31   | Card Management      | Update Card Type                       | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cardholderType                                                                                           |
| 32   | Card Management      | Update Issue Reissue Delivery Option   | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • issueDeliveryOption                                                                                      |
|      |                      |                                        |   • reissueDeliveryOption                                                                                    |
| 33   | Customer Management  | Board Customer                         | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • dualFlag                                                                                                 |
|      |                      |                                        |   • nameTypeIndicator                                                                                        |
|      |                      |                                        |   • residentialFlag                                                                                          |
|      |                      |                                        |   • gender                                                                                                   |
|      |                      |                                        |   • emailAddressFlag                                                                                         |
| 34   | Customer Management  | List Customers' Cards                  | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • gender                                                                                                   |
|      |                      |                                        |   • cardHolderType                                                                                           |
|      |                      |                                        |   • currentCardAction                                                                                        |
|      |                      |                                        |   • lastCardAction                                                                                           |
|      |                      |                                        |   • cardTechnology                                                                                           |
|      |                      |                                        |   • isEcomEnabled                                                                                            |
| 35   | Customer Management  | List Customers' Cards And Accounts     | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • gender                                                                                                   |
| 36   | Customer Management  | Update Customer                        | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • homePhoneFlag                                                                                            |
|      |                      |                                        |   • faxPhoneFlag                                                                                             |
|      |                      |                                        |   • smsFlag                                                                                                  |
|      |                      |                                        |   • mobilePhoneFlag                                                                                          |
|      |                      |                                        |   • phoneFlag                                                                                                |
| 37   | Miscellaneous        | Inquire Business Unit                  | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • transactionBasedOffers                                                                                   |
|      |                      |                                        |   • allowConsolidatedPayments                                                                                |
|      |                      |                                        |   • autoChargebackActive                                                                                     |
|      |                      |                                        |   • actionOnLateFee                                                                                          |
|      |                      |                                        |   • actionOnFinanceCharge                                                                                    |
|      |                      |                                        |   • commercialCardsAllowed                                                                                   |
|      |                      |                                        |   • excludeDefaultDisputedAmounts                                                                            |
|      |                      |                                        |   • earlySettlementQuotesProcess                                                                             |
|      |                      |                                        |   • installmentLoansActive                                                                                   |
| 38   | Product Management   | Inquire Plan Master                    | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • graceBalanceQualification                                                                                |
|      |                      |                                        |   • delinquencyLevelToCancel                                                                                 |
|      |                      |                                        |   • cancellationPlanRollOverMethod                                                                           |
|      |                      |                                        |   • expirationRollover                                                                                       |
|      |                      |                                        |   • expirationPlanRollOverMethod                                                                             |
| 39   | Product Management   | Update Product Card Controls           | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • maximumAuthorizationLimitFrequency                                                                       |
|      |                      |                                        |   • isCountryRiskSpendLimitEnabled                                                                           |
| 40   | Product Management   | Inquire Product                        | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cardProductDisplay                                                                                       |
|      |                      |                                        |   • isLoanFeatureEnabled                                                                                     |
|      |                      |                                        |   • isSameDayEmbossingEnabled                                                                                |
|      |                      |                                        |   • isChipOrPinCardEnabled                                                                                   |
|      |                      |                                        |   • authAlerts                                                                                               |
|      |                      |                                        |   • isSecureCodeEnabled                                                                                      |
|      |                      |                                        |   • isDebitCardProcessEnabled                                                                                |
|      |                      |                                        |   • isTokenizationServiceEnabled                                                                             |
|      |                      |                                        |   • isManualPinResetEnabled                                                                                  |
|      |                      |                                        |   • isCardActionTableEnabled                                                                                 |
|      |                      |                                        |   • defaultCardTechnology                                                                                    |
|      |                      |                                        |   • isScriptingEnabled                                                                                       |
|      |                      |                                        |   • isSweepOptionEnabled                                                                                     |
|      |                      |                                        |   • isCrossBorderAlertEnabled                                                                                |
|      |                      |                                        |   • creditLimitBypass                                                                                        |
|      |                      |                                        |   • isLocalorInternationalUsageEnabled                                                                       |
|      |                      |                                        |   • NewCardDefaultEnabled                                                                                    |
|      |                      |                                        |   • enhancedProductsEligible                                                                                 |
|      |                      |                                        |   • pinMailerNameaddress                                                                                     |
|      |                      |                                        |   • cardMailerNameaddress                                                                                    |
|      |                      |                                        |   • isCardBureauFeedbackEnabled                                                                              |
|      |                      |                                        |   • pinOption                                                                                                 |
|      |                      |                                        |   • isOverlimitProcessingOptionIndicatorEnabled                                                             |
|      |                      |                                        |   • openToBuyCreditBalance                                                                                   |
|      |                      |                                        |   • includeDisputedAmounts                                                                                   |
|      |                      |                                        |   • isWspTokenEnabled                                                                                        |
|      |                      |                                        |   • prepaymentsAllowed                                                                                       |
| 41   | Product Management   | Inquire Product                        | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • interestRounding                                                                                         |
|      |                      |                                        |   • examineCycleInterestVariance                                                                             |
|      |                      |                                        |   • allowNsfPaymentReversal                                                                                  |
|      |                      |                                        |   • yearBase                                                                                                 |
|      |                      |                                        |   • tierLimitIndicator                                                                                       |
|      |                      |                                        |   • rateIndexTable                                                                                           |
|      |                      |                                        |   • isInterestOnFeeEnabled                                                                                   |
|      |                      |                                        |   • transactionQualification                                                                                 |
|      |                      |                                        |   • isWaivePriorDeferredInterestEnabled                                                                      |
|      |                      |                                        |   • isPriorDeferredNsfPaymentReversalEnabled                                                                 |
|      |                      |                                        |   • priorDeferredInterestBalanceIndicator                                                                    |
|      |                      |                                        |   • isPriorDeferredBalanceEnabled                                                                            |
|      |                      |                                        |   • priorDeferredPaidDateQualification                                                                       |
|      |                      |                                        |   • isWaiveCurrentCycleInterestEnabled                                                                       |
|      |                      |                                        |   • isCurrentCycleNsfPaymentReversalEnabled                                                                  |
|      |                      |                                        |   • currentCycleInterestBalanceIndicator                                                                     |
|      |                      |                                        |   • isCurrentCycleBalanceEnabled                                                                             |
|      |                      |                                        |   • currentCyclePaidDateQualification                                                                        |
|      |                      |                                        |   • isWaivePriorCycleInterestEnabled                                                                         |
|      |                      |                                        |   • isPriorCycleNsfPaymentReversalEnabled                                                                    |
|      |                      |                                        |   • priorCycleInterestBalanceIndicator                                                                       |
|      |                      |                                        |   • isPriorCycleBalanceEnabled                                                                               |
|      |                      |                                        |   • isWaiveResidualInterestEnabled                                                                           |
|      |                      |                                        |   • isResidualInterestNsfPaymentReversalEnabled                                                              |
|      |                      |                                        |   • isResidualInterestBalanceEnabled                                                                         |
| 42   | Account Management   | Inquire Behavioural History            | • Type changed from string to integer for below fields                                                       |
|      |                      |                                        |   • cycleDue                                                                                                 |

### Deleted APIs

N/A
