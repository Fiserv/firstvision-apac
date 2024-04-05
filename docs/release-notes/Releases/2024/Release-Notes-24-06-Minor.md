# Release 24.06-Minor - Version 1.9.0

## Date: 13/06/2024

### General Changes
- Restricting auto sign-on IDs from LUI access.

#### Documentation Change in Swagger

- Inquire Account: New field excludeFromVAUOrABUIndicator added in response
- Inquire Account Preference: New field excludeFromVAUOrABUIndicator added in response
- Update Account Preference: New field excludeFromVAUOrABUIndicator added in request and response
- Inquire Account Plan: Label name changed from recordNumber to planSequenceNumber in response, Field values changed from "" to " " for planDescription, referenceNumber, rateType, status and userdefinedPromotionalProductId
- Inquire User Fields : Field values changed from "" to " " for user06 to user12, code03 to code05, code10 to code13
- List Memos : Field values changed from "" to " " for status, referralRepresentativeId, actionNote1 to actionNote5
- Inquire Customer : Field values changed from "" to " " for birthName, middleName, houseNumber
- Update Customer : Field values changed from "" to " " for birthName, middleName, houseNumber
- List Customers' Accounts : Field values changed from "" to " " for addressLine4 and blockCode2
- List Customers' Cards : Field values changed from "" to " " for addressLine4
- List Customers' Cards And Accounts : Field values changed from "" to " " for addressLine4 and blockCode2
- Inquire Business Unit : Field values changed from "" to " " for relationshipAuthorisationActive
- Inquire Plan Master : Field values changed from "" to " " for cancellationLetterId
- Inquire User : Field values changed from "" to " " for servicePrivilegeGroupId, signonExpiryDate, activationDate, businessUnitPrivilegeId
- Update User : Field values changed from "" to " " for servicePrivilegeGroupId, signonExpiryDate, activationDate, businessUnitPrivilegeId
- Transfer Plan Balance: Label name changed from transferFromRecordNumber to transferFromPlanSequenceNumber and transferToRecordNumber to transferToPlanSequenceNumber in request and response
- List Plans: Label name changed from recordCount to planSequenceNumber in response
- Transfer Lost Stolen Card: New field issueDeliveryOption and isSuppressPinEnabled added in request
- Update Issue Reissue Delivery Option: Valid values with description changed for issueDeliveryOption and reissueDeliveryOption in request and response
- Inquire Issue Reissue Delivery Option: Valid values with description changed for issueDeliveryOption and reissueDeliveryOption in response
- Inquire Card: New fields invalidPinDate and invalidPinTime added in response, Field values changed from "" to " " for mobileDeviceID and reasonCode
- Inquire Card Preference: Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response
- Update Card Preference: Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response
- Inquire Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Original Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Loan Schedule: Label installmentConversionFeeAmount changed to instalmentConversionFeeAmount in response and Label name changed from recordNumber to planSequenceNumber in response
- Close Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Plan Controls - Field typeOfLoan type changed to string and description for valid value '0' added for typeOfLoan in response
- Board Entities: accountDirectDebitDetails group with DD related fields added under accountDetails in request
- Board Entities V2: accountDirectDebitDetails group with DD related fields added under accountDetails in request
- Board Account: accountDirectDebitDetails group with DD related fields added under accountDetails in request
- Inquire Direct Debit Controls: paymentChangeDate, requestDays, suspenseStartDate, suspenseEndDate and customerName added in response. Value '9' added in paymentType description in response.
- Update Direct Debit Controls: paymentChangeDate, requestDays, suspenseStartDate, suspenseEndDate and customerName added in request/response. informationalMessage added in response. maxLength updated from 24 to 17 for nominatedPaymentAmountOrPercentage in request. Value '9' added in paymentType enum and it's description in response/request.
- List Billed Transactions: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- List Unbilled Transactions: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- List Outstanding Transactions: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- Inquire Statement Transaction Details: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- List Transactions by Date Range: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- List Transactions by Date Range V2: foreignOriginalAmount and foreignOriginalCurrencyCode added in response
- Bill Payments: settlementDate added in request/response.
- Balance Transfer: settlementDate added in request/response.

### New APIs

#### ApplePay MDES Push Provisioning

This API is used for push provisioning of Master Card. Card push provisioning refers to the creation of a secure digital copy of a preexisting card (either physical or virtual). The copy is then added to a Apple Pay wallet.

#### GooglePay - SamsungPay MDES Push Provisioning

This API is used for push provisioning of Master Card. Card push provisioning refers to the creation of a secure digital copy of a preexisting card (either physical or virtual). The copy is then added to a GooglePay or SamsungPay wallet.

### Updated APIs

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | Inquire Account | <ul> <li> New field excludeFromVAUOrABUIndicator added in response |
| 2 | Account Management | Inquire Account Preference | <ul> <li> New field excludeFromVAUOrABUIndicator added in response |
| 3 | Account Management | Update Account Preference | <ul> <li> New field excludeFromVAUOrABUIndicator added in request and response |
| 4 | Account Management | Inquire Account Plan | <ul> <li> Label name changed from recordNumber to planSequenceNumber in response |
| 5 | Account Management | Transfer Plan Balance | <ul> <li> Label name changed from transferFromRecordNumber to transferFromPlanSequenceNumber and transferToRecordNumber to transferToPlanSequenceNumber in request and response|
| 6 | Account Management | List Plans | <ul> <li> Label name changed from recordCount to planSequenceNumber in response |
| 7 | Card Management | Transfer Lost Stolen Card | <ul> <li> New field issueDeliveryOption and isSuppressPinEnabled added in request |
| 8 | Card Management | Update Issue Reissue Delivery Option | <ul> <li> Valid values with Description changed for issueDeliveryOption and reissueDeliveryOption in request and response |
| 9 | Card Management | Inquire Issue Reissue Delivery Option | <ul> <li> Valid values with Description changed for issueDeliveryOption and reissueDeliveryOption in request and response |
| 10 | Card Management | Inquire Card | <ul> <li> New field invalidPinDate and invalidPinTime added in response |
| 11 | Card Management | Inquire Card Preference| <ul> <li> Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response |
| 12 | Card Management | Update Card Preference| <ul> <li> Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response |
| 13 | Loan Management | Inquire Loan | <ul> <li> Label name changed from recordNumber to planSequenceNumber in response |
| 14 | Loan Management | Inquire Loan Schedule | <ul> <li> Label installmentConversionFeeAmount changed to instalmentConversionFeeAmount in response </li> <li> Label name changed from recordNumber to planSequenceNumber in response |
| 15 | Loan Management | Close Loan | <ul> <li> Label name changed from recordNumber to planSequenceNumber in response |
| 16 | Loan Management | Inquire Plan Controls | <ul> <li> Field typeOfLoan type changed to string </li> <li> New value '0' added in description for typeOfLoan in response |
| 17 | Miscellaneous | Board Entities | <ul> <li> accountDirectDebitDetails group with DD related fields added under accountDetails in request |
| 18 | Miscellaneous | Board Entities V2 | <ul> <li> accountDirectDebitDetails group with DD related fields added under accountDetails in request |
| 19 | Account Management | Board Account | <ul> <li> accountDirectDebitDetails group with DD related fields added under accountDetails in request |
| 20 | Account Management | Inquire Direct Debit Controls | <ul> <li> paymentChangeDate, requestDays, suspenseStartDate, suspenseEndDate and customerName added in response </li> <li> Value '9' added in paymentType description in response |
| 21 | Account Management | Update Direct Debit Controls | <ul> <li> paymentChangeDate, requestDays, suspenseStartDate, suspenseEndDate and customerName added in request/response. </li> <li> informationalMessage added in response. </li> <li> maxLength updated from 24 to 17 for nominatedPaymentAmountOrPercentage in request. </li> <li> Value '9' added in paymentType enum and it's description in response/request |
| 22 | Account Management | List Billed Transactions | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 23 | Account Management | List Outstanding Authorizations | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 24 | Account Management | List Unbilled Transactions | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 25 | Account Management | Inquire Statement Transaction Details | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 26 | Account Management | List Transactions by Date Range | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 27 | Account Management | List Transactions by Date Range V2 | <ul> <li> foreignOriginalAmount and foreignOriginalCurrencyCode added in response |
| 28 | Authorizations | Bill Payments | <ul> <li> settlementDate added in request/response |
| 29 | Authorizations | Balance Transfer | <ul> <li> settlementDate added in request/response |

### Deleted APIs

N/A
