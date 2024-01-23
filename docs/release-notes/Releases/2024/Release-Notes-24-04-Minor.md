# Release 24.04-Minor - Version 1.8.0

## Date: 11/04/2024

### General Changes

#### Documentation Change in Swagger

- Board Entities: New value ‘2’ added in isDynamicCVV2enabled field in request
- Board Entities V2: New value ‘2’ added in isDynamicCVV2enabled field in request
- Board Card: New value ‘2’ added in isDynamicCVV2enabled field in request
- Inquire Card: New value ‘2’ added in isDynamicCVV2enabled field in response
- Inquire Card Preference: New value ‘2’ added in isDynamicCVV2enabled field in response
- Update Card Preference: New value ‘2’ added in isDynamicCVV2enabled field in request and response
- List Billed Transactions: merchantName added in response and existing merchantCity length updated to 13 from 15 in response
- List Unbilled Transactions: merchantName added in response and existing merchantCity length updated to 13 from 15 in response
- List Outstanding Transactions: merchantName added in response and existing merchantCity length updated to 13 from 15 in response
- Inquire Statement Transaction Details: merchantName added in response and existing merchantCity length updated to 13 from 15 in response
- List Transactions by Date Range: merchantName added in response and existing merchantCity length updated to 13 from 15 in response
- Statement Balance Simulation - maxLength has been changed from 5 to 30 for planIdDescription in response
- Statement Balance Conversion - maxLength has been changed from 5 to 30 for planIdDescription in response

### New APIs

#### Inquire Payoff Quote

This API is used to fetch Instalment plan balance and pro rata interest that would be charged in case the customer wants to close a Loan plan on a given date.

#### List Transactions by Date Range V2

This API is used to fetch the list of various transactions like authorizations, memos, outstanding authorizations, unbilled and billed transactions for a given date range and account Id.

### Updated APIs

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Miscellaneous | Board Entities | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in request |
| 2 | Miscellaneous | Board Entities V2 | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in request |
| 3 | Card Management | Board Card | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in request |
| 4 | Card Management | Inquire Card | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in response |
| 5 | Card Management | Inquire Card Preference | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in response |
| 6 | Card Management | Update Card Preference | <ul> <li> New value ‘2’ added in isDynamicCVV2enabled field in request and response|
| 7 | Product Management | Inquire Product | <ul> <li> isDynamicCVV2enabled added in response |
| 8 | Loan Management | Inquire Plan Controls | <ul> <li> billingIndicator added in response |
| 10 | Account Management | List Billed Transactions | <ul> <li> merchantName added in response </li> <li> Existing field merchantCity length updated to 13 from 15 in response |
| 11 | Account Management | List Outstanding Authorizations | <ul> <li> merchantName added in response </li> <li> Existing field merchantCity length updated to 13 from 15 in response |
| 12 | Account Management | List Unbilled Transactions | <ul> <li> merchantName added in response </li> <li> Existing field merchantCity length updated to 13 from 15 in response |
| 13 | Account Management | Inquire Statement Transaction Details | <ul> <li> merchantName added in response </li> <li> Existing field merchantCity length updated to 13 from 15 in response |
| 14 | Account Management | List Transactions by Date Range | <ul> <li> merchantName added in response </li> <li> Existing field merchantCity length updated to 13 from 15 in response |

### Deleted APIs

N/A
