# Release 24.08-Minor - Version 1.10.0

## Date: 13/08/2024

### General Changes

- NA

#### Documentation Change in Swagger

- Inquire Account: New field balanceTransferOutstandingAmount under amountDetails added in response
- Inquire Plan Master: New fields balanceTransferFeeType and balanceTransferFeeAmountOrPercentage added in response
- List Billed Transactions: New field acquirerReferenceNumber added in response
- List Unbilled Transactions: New field acquirerReferenceNumber added in response
- List Outstanding Authorizations: New field acquirerReferenceNumber added in response
- Inquire Statement Transaction Details: New field acquirerReferenceNumber added in response
- List Transactions by Date Range: New field acquirerReferenceNumber added in response
- List Transactions by Date Range V2: New field acquirerReferenceNumber added in response
- Inquire Delinquency - Existing fields deleted (previousCycleDue, lastDelinquentDate and paymentDaysDelinquentCount) and restructured the API response (delinquencyDetails renamed to accountDueDetails, accountDetails and reageControls groups were added, and new fields planTotalDueAmount and differenceInTotalAmount added) 

### New APIs

#### Inquire Account Limits

This API provides daily maximum cash deposit authorization amount and count allowed for a given accountId.

#### Update Account Limits

This API allows user to set daily maximum cash deposit authorization amount and count for a given accountId.

#### Inquire Account Statistics

This API provides daily accumulated cash deposite authorization amount and count for the given accountId.

#### Update Delinquency

This service is used to reage the account, reaging an account is normally done to cause an account to appear less delinquent by reducing the delinquency level. Also, user can adjust the account level due buckets or plan level dues if there is any discrepancy.

### Updated APIs -

| S.No | Category            | API Name                               | Change                                                                                              |
|------|---------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1    | Account Management  | Inquire Account                        | • New field balanceTransferOutstandingAmount added in response                                      |
| 2    | Account Management  | List Billed Transactions                | • New field acquirerReferenceNumber added in response                                               |
| 3    | Account Management  | List Outstanding Authorizations         | • New field acquirerReferenceNumber added in response                                               |
| 4    | Account Management  | List Unbilled Transactions              | • New field acquirerReferenceNumber added in response                                               |
| 5    | Account Management  | Inquire Statement Transaction Details   | • New field acquirerReferenceNumber added in response                                               |
| 6    | Account Management  | List Transactions by Date Range         | • New field acquirerReferenceNumber added in response                                               |
| 7    | Account Management  | List Transactions by Date Range V2      | • New field acquirerReferenceNumber added in response                                               |
| 8    | Product Management  | Inquire Plan Master                     | • New fields balanceTransferFeeType and balanceTransferFeeAmountOrPercentage added in response       |
| 9 | Account Management | Inquire Delinquency | • previousCycleDue, lastDelinquentDate and paymentDaysDelinquentCount are deleted from response.  • Restructured the API response (delinquencyDetails renamed to accountDueDetails, accountDetails and reageControls groups were added, and new fields planTotalDueAmount and differenceInTotalAmount added)' |


### Deleted APIs

N/A
