# Release 24.02-Minor - Version 1.7.0

## Date: 26/02/2024

### General Changes

#### Idempotency changes in POST APIs

When a client sends a POST request, it can include a Idempotency key in the request headers. The server can use this key to identify duplicate requests and ensure that the request is processed only once. On the server side, you can check the idempotency key and ensure that the request processing is idempotent.  And as the server receives a duplicate request, it can respond with the result of the original request instead of reprocessing it. Client can intercept this response and avoid repeating the same operation

#### Documentation Change in Swagger

- POST APIs: New http response code '409' added for all POST APIs
- Inquire MCC Limits: maxLength has been changed from 11 to 18 for all amount fields in response
- Update MCC Limits: maxLength has been changed from 11 to 18 for all amount fields in response
- Inquire Loan: label change from celEppManualClose to manualCloseIndicator
- Board Card: externalContractId length updated from 14 to 19 in request
- Board Account: externalContractId length updated from 14 to 19 in request
- Board Entities: externalContractId length updated from 14 to 19 in request
- Board Entities V2: externalContractId length updated from 14 to 19 in request
- Inquire Card: externalContractId length updated from 14 to 19 in response
- Inquire Account: externalContractId length updated from 14 to 19 in response
- List Customers Cards and Accounts: externalContractId length updated from 14 to 19 in response under accountDetails
- List Customers Accounts: externalContractId length updated from 14 to 19 in response
- List External Customers Cards and Accounts: externalContractId (path variable) length updated from 14 to 19 in response
- Request Authorization: internalReferenceNumber type has changed from integer to string
- Reverse Authorization: internalReferenceNumber type has changed from integer to string


### New APIs

#### Inquire Plan Controls

This API is used to fetch loan plan details for a given plan Id.

#### Inquire Instalment Offers

This API is used to fetch instalment offers for a given loan plan id, Loan Amount and account id.

#### Inquire Transaction Instalment Details

This API is used to fetch details of all transaction instalment loans against an account.

#### List Loans By Account

This API is used to fetch list of loans associated with an account id given.

#### List Statement Eligible Plan Balance

This API is used to fetch all the plan segments eligible for SIP conversion. The Loan conversion Eligibility for the Plan will be checked and only qualifying plans and balances will be listed.

#### List Transaction Instalments

This API is used to fetch details of all transaction instalment loans against an account.

#### Close Loan

This API is used to close a specific loan manually for a given account Id.

#### Cash Balance Conversion

This API is used to validate if the Cash balance conversion is allowed for given account. This API will be created to cater to Conversion steps, depending on the Type of Request.

#### Cash Balance Simulation

This API is used to validate if the Cash balance simulation is allowed for given account. This API will be created to cater Simulation steps, depending on the Type of Request.

#### Statement Balance Conversion

This API is used to convert statement balance into Instalment. API first validates the given plans are eligible for statement balance conversion, if eligible then system converts into instalment for the requested term and also responds with loan scheduling details.

#### Statement Balance Simulation

This API is used to validate if given plans are eligible for statement balance conversion, if eligible then system responds with loan scheduling details.

#### Transaction Instalment Simulation

This API is used to validate if given transactions are eligible to convert into instalment. If transactions are eligible for conversion, then response will show the loan scheduling details.

#### Transaction Instalment Conversion

This API supports both single and multiple transaction conversion into instalments. API first validates if given transactions are eligible to convert into instalment. If transactions are eligible, then system converts given transactions into instalment.

#### Balance Transfer

This API is used to make an authorization request for payment instrument Id or payment card number when transaction for Balance Transfer.

#### Bill Payments

This API is used to make an authorization request for payment instrument Id or payment card number when transaction for Bill Payment.

#### Validate CVV2 V2

This API is used to validate the encrypted CVV2 for a given payment instrument Id.

### Updated APIs

| S.No | Category            | API Name                               | Change                                                                                              |
|------|---------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------|
| 1    | Account Management  | Board Account                          | • externalContractId length updated to 19 in response                                               |
| 2    | Account Management  | Inquire Account                        | • externalContractId length updated to 19 in response                                               |
| 3    | Card Management     | Board Card                             | • externalContractId length updated to 19 in response                                               |
| 4    | Miscellaneous       | Board Entities                         | • externalContractId length updated to 19 in response                                               |
| 5    | Miscellaneous       | Board Entities V2                      | • externalContractId length updated to 19 in response                                               |
| 6    | Card Management     | Inquire Card                           | • externalContractId length updated to 19 in response  • pinDetails group added in response                                                                |
| 7    | Customer Management | List Customers Accounts                | • externalContractId length updated to 19 in response                                               |
| 8    | Customer Management | List Customers Cards                   | • externalContractId added under cardList in response                                               |
| 9    | Customer Management | List Customers Cards and Accounts      | • externalContractId length updated to 19 in response  • externalContractId added under cardList in response                                               |
| 12   | Account Management  | Monetary Action                        | • transactionDescription added in request                                                           |
| 14   | Account Management  | List Billed Transactions                | • billerCode added in response                                                                      |
| 15   | Account Management  | List Outstanding Authorizations         | • billerCode added in response                                                                      |
| 16   | Account Management  | List Unbilled Transactions              | • billerCode added in response  • instalmentConversionInd added in response                                                         |
| 17   | Account Management  | Inquire Statement Transaction Details   | • billerCode added in response                                                                      |
| 18   | Account Management  | List Transaction by Date range          | • billerCode added in response                                                                      |
| 19   | Product Management  | Inquire Product                        | • instalmentDetails group added in response                                                         |
| 20   | Miscellaneous       | Inquire Business Unit                  | • instalmentDetails group added in response                                                         |
| 21   | Card Management     | Transfer Lost and Stolen               | • pinStatus added in response                                                                       |
| 22   | Loan Management     | Inquire Loan                           | • label change from celEppManualClose to manualCloseIndicator  • prorateInterestAmout added under group loanDisclosedAndInitialAmountDetails                         |
| 23   | Account Management  | Inquire Account Plan                   | • eligibleBalanceForStatementInstalment added in response                                           |
| 24   | Card Management     | Inquire MCC Limits                     | • maxLength for the amount fields changed from 11 to 18 in response                                 |
| 25   | Card Management     | Update MCC Limits                      | • maxLength for the amount fields changed from 11 to 18 in response                                 |
| 26   | Account Management  | Transfer Plan Balance                  | • API extended to support partial plan balance and reversal                                         |
| 27   | Customer Management | List External Customers Cards and Accounts | • externalContractId length updated to 19 in request (path variable) and response                    |
| 28   | Authorizations      | Request Authorization                  | • internalReferenceNumber type has changed from integer to string in response                        |
| 29   | Authorizations      | Reverse Authorization                  | • internalReferenceNumber type has changed from integer to string in response                        |

### Deleted APIs

N/A
