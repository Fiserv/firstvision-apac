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

| S.No | Category            | API Name                | Change                                                                                             |
|------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------|
| 1    | Account Management  | Inquire Account         | • New field cycleDue and defaultPlanDetails group added in response                                |
| 2    | Account Management  | List Plans              | • New field calculatedInterestRate, lastInterestRate and planType added in response                |
| 3    | Account Management  | Update Waive Fees       | • New enum value 2 added in isWaiveInterestFeeEnabled and isWaiveAddOnMembershipFeeEnabled  • New enum value 4 added in isWaiveAnnualMembershipFeeEnabled                                      |
| 4    | Card Management     | Inquire Card            | • New field isVAUAndABUEnabled and updateVAUAndABUDate added in response                           |
| 5    | Card Management     | Inquire Card Preference | • New field isVAUAndABUEnabled and updateVAUAndABUDate added in response                           |
| 6    | Card Management     | Update Card Preference  | • New field isVAUAndABUEnabled added in request   • isVAUAndABUEnabled and updateVAUAndABUDate added in response                                     |
| 7    | Card Management     | Activate Card           | • Changes to update new crypto keys on back of card activation                                     |
| 8    | Card Management     | List Tokens             | • API name has been changed to List Tokens  • label vtsTokenNumber is changed to schemeTokenNumber  • endPoint is updated from /listVisaToken to /listTokens                                           |

### Deleted APIs

N/A
