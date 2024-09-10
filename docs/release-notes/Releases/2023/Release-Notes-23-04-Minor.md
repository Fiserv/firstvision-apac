## Markdown Header
# Release 23.04-Minor - Version 1.2.0

## Date: 14/04/2023

### General Changes

#### Documentation Change in Swagger

- Board Account/Board Entities/Product Transfer/Transfer Lost Stolen Card : Example changed for all date fields in request body from '0' to '00/00/0000'
- Update Issue Reissue Delivery Option : Example added for startDate and effectiveDate in request body from '00/00/000' to '00/00/0000'
- Push Provisioning : API name has been changed to ‘ApplePay push Provisioning’ and typo correction for Authentification field
- Inquire Customer/Update Customer/List Customers’ Cards/List Customers’ Cards and Accounts/List Customers’ Accounts: Description modified for Business Unit
- Inquire Interest Table : maxLength updated for variance1-9 from 7 to 10 (This is rate field and not suffixed with 'rate' in label)
- Inquire Service Charge Table : maxLength updated for singleFeeMinimum/maximumAmount from 9 to 16 and example updated.
- All APIs : API description modified

### New APIs

NA

### Updated APIs

| S.No | Category             | API Name                               | Change                                                                                                        |
|------|----------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 1    | Account Management   | Inquire statement transaction          | • Changed Statement Date mandatory to optional in input request                                               |
| 2    | Account Management   | Inquire statement plan details         | • Changed Statement Date mandatory to optional in input request                                               |
| 3    | Account Management   | List Billed Transactions               | • Added memoDebitOrCreditIndicator in response                                                                |
| 4    | Account Management   | List Unbiiled Transactions             | • Added memoDebitOrCreditIndicator in response                                                                |
| 5    | Account Management   | Inquire Statement Transactions         | • Added memoDebitOrCreditIndicator in response                                                                |
| 6    | Account Management   | List Outstanding Auths                 | • Added memoDebitOrCreditIndicator in response                                                                |
| 7    | Account Management   | List Transactions by Date Range        | • Added memoDebitOrCreditIndicator in response                                                                |
| 8    | Account Management   | Update Direct Debit Controls           | • Label name and length changes for below fields in request and response • nominatedAmount to nominatedPaymentAmountOrPercentage  • Enum value '1' of paymentRemittanceMethod deleted                                                         |
| 9    | Account Management   | Inquire Direct Debit Controls          | • Label name and length changes for below fields in response  • nominatedAmount to nominatedPaymentAmountOrPercentage  • Enum value '1' of paymentRemittanceMethod deleted                                                         |
| 10   | Account Management   | Inquire Account                        | • Added creditLimitChangeDate in response                                                                     |
| 11   | Authorization        | Request Authorization                  | • Added EffectiveDate in response                                                                             |
| 12   | Authorization        | Reverse Authorization                  | • Added EffectiveDate in response                                                                             |
| 13   | Authorization        | Inquire Authorization                  | • Added EffectiveDate in response                                                                             |
| 14   | Card Management      | ApplePay Push Provisioning             | • Changed businessUnit mandatory to optional in input request                                                 |
| 15   | Card Management      | GooglePay - SamsungPay VTS Push Provisioning | • Changed businessUnit mandatory to optional in input request                                             |
| 16   | Card Management      | Inquire Dynamic CVV2                   | • Changed businessUnit mandatory to optional in input request                                                 |
| 17   | Card Management      | Generate Dynamic CVV2                  | • Changed businessUnit mandatory to optional in input request                                                 |
| 18   | Card Management      | Change Pin                             | • Added below fields in request  • pinSetOrResetActionCode  • pinSetOrResetMemo  • pinTryCounterResetActionCode  • pinTryCounterResetMemo                                                                                    |
| 19   | Customer Management  | List Customers' Cards and Accounts     | • Restructured the responseBody as per backend changes • New accountList Group added in service • New accountId field added in existing cardList group                                                      |
| 20   | Customer Management  | Inquire Customer                       | • Added below fields in response  • county  • externalId   • typeOfExternalId  • phoneExtension  • vacationDetails added as a group                                                                          |
| 21   | Customer Management  | Update Customer                        | • Added below fields in request and response  • county  • externalId  • typeOfExternalId  • phoneExtension  • vacationDetails added as a group                                                                          |
| 22   | Miscellaneous        | Board Entities                         | • Changed owningBranchNumber mandatory to optional in input request                                           |
| 23   | All API's            | NA                                     | • Error message status changed for all functional API's from 422 to 404 for invalid path when record is not available in First Vision |

### Deleted APIs

N/A
