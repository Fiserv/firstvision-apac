# Release 24.06-Minor - Version 1.9.0

## Date: 13/06/2024

### General Changes

#### Documentation Change in Swagger

- Inquire Account: New field excludeFromVAUOrABUIndicator added in response
- Inquire Account Preference: New field excludeFromVAUOrABUIndicator added in response
- Update Account Preference: New field excludeFromVAUOrABUIndicator added in request and response
- Inquire Account Plan: Label name changed from recordNumber to planSequenceNumber in response
- Transfer Plan Balance: Label name changed from transferFromRecordNumber to transferFromPlanSequenceNumber and transferToRecordNumber to transferToPlanSequenceNumber in request and response
- List Plans: Label name changed from recordCount to planSequenceNumber in response
- Transfer Lost Stolen Card: New field issueDeliveryOption and isSuppressPinEnabled added in request
- Update Issue Reissue Delivery Option: Valid values with description changed for issueDeliveryOption and reissueDeliveryOption in request and response
- Inquire Issue Reissue Delivery Option: Valid values with description changed for issueDeliveryOption and reissueDeliveryOption in response
- Inquire Card: New fields invalidPinDate and invalidPinTime added in response
- Inquire Card Preference: Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response
- Update Card Preference: Field values with description changed for issueDeliveryOption and reissueDeliveryOption field in response
- Inquire Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Original Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Loan Schedule: Label installmentConversionFeeAmount changed to instalmentConversionFeeAmount in response and Label name changed from recordNumber to planSequenceNumber in response
- Close Loan: Label name changed from recordNumber to planSequenceNumber in response
- Inquire Plan Controls - Field typeOfLoan type changed to string and description for valid value '0' added for typeOfLoan in response

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

### Deleted APIs

N/A
