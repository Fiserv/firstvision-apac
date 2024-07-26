# Release 24.10-Minor - Version 1.11.0

## Date: 17/10/2024

### General Changes

- NA

#### Documentation Change in Swagger

- Inquire Account: New field cycleDue and defaultPlanDetails group added in response
- List Plans: New field calculatedInterestRate, lastInterestRate and planType added in response
- Inquire Card: New field isVAUAndABUEnabled and updateVAUAndABUDate added in response
- Inquire Card Preference: New field isVAUAndABUEnabled and updateVAUAndABUDate added in response
- Update Card Preference: New field isVAUAndABUEnabled added in request and isVAUAndABUEnabled, updateVAUAndABUDate added in response.
- List Visa Token: API name has been changes to List Tokens, label vtsTokenNumber is changed to schemeTokenNumber, endPoint is also updated from /listVisaToken to /listTokens.

### New APIs

#### Cash Advance

This API provides daily maximum cash deposit authorization amount and count allowed for a given accountId.

#### Cash Deposit

This API allows user to set daily maximum cash deposit authorization amount and count for a given accountId.

#### Inquire Account Fees and Controls

This API provides daily accumulated cash deposite authorization amount and count for the given accountId.

### Updated APIs -

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | Inquire Account | <ul> <li> New field cycleDue and defaultPlanDetails group added in response |
| 2 | Account Management | List Plans | <ul> <li> New field calculatedInterestRate, lastInterestRate and planType added in response |
| 3 | Account Management | Update Waive Fees | <ul> <li> New enum value 2 added in isWaiveInterestFeeEnabled and isWaiveAddOnMembershipFeeEnabled </li> <li> New enum value 4 added in isWaiveAnnualMembershipFeeEnabled |
| 4 | Card Management | Inquire Card | <ul> <li> New field isVAUAndABUEnabled and updateVAUAndABUDate added in response |
| 5 | Card Management | Inquire Card Preference | <ul> <li> New field isVAUAndABUEnabled and updateVAUAndABUDate added in response |
| 6 | Card Management | Update Card Preference | <ul> <li> New field isVAUAndABUEnabled added in request </li> <li> isVAUAndABUEnabled, updateVAUAndABUDate added in response |
| 7 | Card Management | Activate Card | <ul> <li> Changes to update new crypto keys on back of card activation |
| 8 | List Tokens | Card Management | <ul> <li> API name has been changes to List Tokens </li> <li> label vtsTokenNumber is changed to schemeTokenNumber </li> <li> endPoint is updated from /listVisaToken to /listTokens |


### Deleted APIs

N/A
