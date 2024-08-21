# Release 23.06-Minor - Version 1.3.0

## Date: 14/06/2023

### General Changes

- Amount/Credit limit validation added in API transformation layer for below APIs
  - Board Account
  - Board Entity
  - Update Spend Limit
  - Update Credit Limit
  - Update Temporary Credit Limit

- Changes to include $ symbol for all amount fields in response for all APIs.

#### Documentation Change in Swagger

- Inquire Authorization: Type changed from string to integer for businessUnit in response
- ApplePay/GooglePay Push Provisioning: Updated the mandatory fields in request as per VISA guidelines
- Inquire Service Charge Table: Label name changed for tier1Fee and tier2Fee to tier1FeeAmountOrPercentage and tier2FeeAmountOrPercentage respectively, also example value has been updated for the same fields.
- Inquire/Update Direct Debit Controls: Example corrected for nominatedPaymentAmountOrPercentage
- Inquire Statement Transaction Details: maxLength changed from 13 to 3 and type changed from string to integer for merchantBusinessUnit field in response
- Reverse Authorization: Type changed from string to integer for responseCode in response
- Get Access Token: Description updated for scope
- Update Card Action: Description updated for cardActionDate

### New APIs

#### Inquire BNPL Controls

This API is used to inquire BNPL controls at account level for a given account id.

#### Inquire Direct Debit Controls

This API is used to inquire BNPL direct debit controls at account level for a given account id.

#### Inquire iPlan Details

This API is used to fetch iPlan details for a given account Id.

#### Inquire Offer Code

This API is used to fetch offer code details for a given business unit, product Id and offer code.

#### List iPlans

This API is used to fetch list of iPlans associated with an account Id.

#### List Offer Codes

This API is used to fetch the list of offer codes associated for a given business unit and product Id.

### Updated APIs

| S.No | Category             | API Name                               | Change                                                                                                        |
|------|----------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 1    | Account Management   | List Transactions by Date Range        | • Added below fields in response                                                                              |
|      |                      |                                        |   • merchantCountry                                                                                           |
|      |                      |                                        |   • upiMerchantId                                                                                             |
| 2    | Account Management   | Inquire Statement Transaction details  | • Added bnplIplanSequenceNumber in response                                                                   |
|      |                      |                                        | • Deleted below fields in response                                                                            |
|      |                      |                                        |   • totalDueBalance                                                                                           |
|      |                      |                                        |   • minimumPaymentAmount                                                                                      |
|      |                      |                                        |   • currencyConversionRate                                                                                    |
| 3    | Account Management   | Inquire Statement Plan Details         | • Deleted below fields in response                                                                            |
|      |                      |                                        |   • totalDueBalance                                                                                           |
|      |                      |                                        |   • minimumPaymentAmount (outside plan table)                                                                 |
|      |                      |                                        |   • currencyConversionRate                                                                                    |
| 4    | Account Management   | List Billed Transactions               | • Added bnplIplanSequenceNumber in response                                                                   |
| 5    | Account Management   | List Outstanding Authorizations        | • Added bnplIplanSequenceNumber in response                                                                   |
| 6    | Account Management   | List Unbilled Transactions             | • Added bnplIplanSequenceNumber in response                                                                   |
| 7    | Account Management   | Inquire Account                        | • Added new bnplDetails group in response for BNPL functionality                                              |
|      |                      |                                        | • currencyCode in response has been updated to make the type as string and to get the value "036" instead of "36"   |
| 8    | Account Management   | Board Account                          | • Added new bnplDetails group in request for BNPL functionality                                               |
| 9    | Account Management   | Monetary Action                        | • Type changed from string to integer in requestBody for businessUnit                                         |
| 10   | Account Management   | Post Payments                          | • Type changed from string to integer in requestBody for businessUnit                                         |
| 11   | Account Management   | Add Memo Line                          | • Type changed from string to integer in requestBody for businessUnit                                         |
| 12   | Card Management      | Inquire Card                           | • Added below fields in response                                                                              |
|      |                      |                                        |   • transferToPaymentInstrumentId                                                                             |
|      |                      |                                        |   • transferFromPaymentInstrumentId                                                                           |
| 13   | Customer Management  | List External Customers' Cards and Accounts | • Added below fields in response                                                                          |
|      |                      |                                        |   • transferToPaymentInstrumentId                                                                             |
|      |                      |                                        |   • transferFromPaymentInstrumentId                                                                           |
|      |                      |                                        |   • maskedPaymentCardNumber                                                                                   |
| 14   | Product Management   | Inquire Product                        | • Added new bnplAlerts, bnplDetails, bnplTierRangeOfTemplateId groups in response                             |
| 15   | Miscellaneous        | Board Entities                         | • Added new bnplDetails group in request for BNPL functionality                                               |
| 16   | Miscellaneous        | Inquire Business Unit                  | • Added new field isBnplEnabled in response                                                                   |

### Deleted APIs

N/A
