# Inquire Loan

This service provides Loan detail of customer like Loan disclosed and initial amount of loan, loan disbrusement details, loan topup redraw can restructure detail, fixed interest and skip payment details.

## Endpoint

`GET /v1/loans/{accountId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable and Record number sent as Query Parameter.***


<!--
type: tab
-->

```json

{
  "FixedIntrestDetails": {
    "interestIndicator": 0,
    "interestRate": "0.00000%",
    "nextInterestEffectiveDate": "00/00/0000",
    "nextInterestRate": "0.00000%"
  },
  "accountId": "0006000011000000509",
  "businessUnit": 600,
  "capIndicatorDetails": {
    "isInsuranceCapIndicatorEnabled": "0",
    "isInterestCapIndicatorEnabled": "0",
    "isUserFee1CapIndicatorEnabled": "0",
    "isUserFee2CapIndicatorEnabled": "0",
    "isUserFee3CapIndicatorEnabled": "0",
    "isUserFee4CapIndicatorEnabled": "0",
    "isUserFee5CapIndicatorEnabled": "0",
    "isUserFee6CapIndicatorEnabled": "0"
  },
  "componentCalculationIndicatorDetails": {
    "insuranceIndicator": "3",
    "interestIndicator": "3",
    "userFee1Indicator": "3",
    "userFee2FlagIndicator": "3",
    "userFee3Indicator": "3",
    "userFee4Indicator": "3",
    "userFee5Indicator": "3",
    "userFee6Indicator": "3"
  },
  "disbrusementCreditDetails": {
    "accountIndicator": 0,
    "bankId": "0",
    "disbursementAccountId": "",
    "disbursementDate": "00/00/0000"
  },
  "initializedAmountDetails": {
    "insuranceAmount": "$0.00",
    "interestAmount": "$100.00",
    "loanAmount": "$1,500.00",
    "principalAmount": "$1,400.00",
    "user1Amount": "$0.00",
    "user2Amount": "$0.00",
    "user3Amount": "$0.00",
    "user4Amount": "$0.00",
    "user5Amount": "$0.00",
    "user6Amount": "$0.00"
  },
  "loanDisclosedAndInitialAmountDetails": {
    "billingTerm": 1,
    "celEppCloseFee": "0",
    "celEppManualClose": "0",
    "celEppUser": "",
    "closeReason": "0",
    "currentFinalPaymentAmount": "$500.00",
    "currentTerm": 1,
    "depositAmount": "$0.00",
    "dispersalMethod": "0",
    "finalPaymentDate": "00/00/0000",
    "firstPaymentAmount": "$500.00",
    "firstPaymentDate": "20/09/2021",
    "fixedInterestAmount": "$0.00",
    "initialTerm": 3,
    "lifeToDateNetSalesAmount": "$1,400.00",
    "loanAgreementDate": "17/08/2021",
    "paymentDateChangeCount": 0,
    "planId": 70003,
    "remainingTerm": 2
  },
  "originalDisclosedAmountDetails": {
    "insuranceAmount": "$0.00",
    "interestAmount": "$100.00",
    "loanAmount": "$1,500.00",
    "principalAmount": "$1,400.00",
    "user1Amount": "$0.00",
    "user2Amount": "$0.00",
    "user3Amount": "$0.00",
    "user4Amount": "$0.00",
    "user5Amount": "$0.00",
    "user6Amount": "$0.00"
  },
  "recordNumber": 1,
  "skipPaymentDetails": {
    "lastSkipPaymentDate": "00/00/0000",
    "lifeToDateSkipPaymentCount": 0,
    "skipPaymentIndicator": "0",
    "yearToDateSkipPaymentCount": 0
  },
  "topUpRedrawCanRestructureDetails": {
    "cancelExpiryDate": "00/00/0000",
    "lastFixedPaymentAmount": "$0.00",
    "lastFixedPaymentMaintenanceDate": "00/00/0000",
    "lastRedrawAmount": "$0.00",
    "lastRedrawRequestDate": "00/00/0000",
    "lastRestructureDate": "00/00/0000",
    "lastTerm": 0,
    "lastTermMaintenanceDate": "00/00/0000",
    "lastTopUpAmount": "$0.00",
    "lastTopUpRequestDate": "00/00/0000",
    "redrawExpiryDate": "00/00/0000",
    "restructureLetterId": "",
    "restructureReason": "0",
    "topUpExpiryDate": "30/11/2000"
  }
}

```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/loans/0006000011000000509/details",
    "invalid-params": [
      "V5PS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|
| `recordNumber` | Query Parameter | *integer*| 3 | Record number that identifies each Credit Plan Segment record assigned to the account. The values are 0–999. The value 0 indicates a “phantom” plan used to disclose interest rates when no cash or retail plan exists for an account.|


### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PS0004SF` | Get request - Record not Found |  
| `V5PS4411SA` | Account not present in ambs file |  
| `V5PS4411SB` | Amps - plan data record not found | 
| `V5PS4410SB` | Org record not present | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*