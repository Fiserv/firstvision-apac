# Inquire Original Loan

This API is used to fetch existing loan plan records. It contains the original precomputed amounts and other original information received for a loan plan for a given account Id.

## Endpoint

`GET /v1/loans/{accountId}/originalDetails`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable and plan sequence number sent as Query Parameter.***

<!--
type: tab
-->

```json
{
  "accountId": "0006000011000000509",
  "amountDetails": {
    "depositAmount": "$0.00",
    "finalPaymentAmount": "$500.00",
    "firstPaymentAmount": "$500.00",
    "insuranceAmount": "$0.00",
    "interestAmount": "$100.00",
    "interestFlatAmount": "$0.00",
    "principalAmount": "$1,400.00",
    "userFee1Amount": "$0.00",
    "userFee2Amount": "$0.00",
    "userFee3Amount": "$0.00",
    "userFee4Amount": "$0.00",
    "userFee5Amount": "$0.00",
    "userFee6Amount": "$0.00"
  },
  "annualPercentageRate": "0.35000%",
  "billingDefermentDetails": {
    "billingPeriod": 0,
    "billingStartDate": "00/00/0000",
    "billingTermIndicator": "0"
  },
  "billingTerm": 1,
  "businessUnit": 600,
  "dateDetails": {
    "agreementDate": "17/08/2021",
    "finalPaymentDate": "00/00/0000",
    "firstPaymentDate": "20/09/2021",
    "openDate": "17/08/2021"
  },
  "dispersalMethod": "0",
  "initialRebateDetails": {
    "initialInsuranceRebateIndicator": 0,
    "initialInterestRebateIndicator": 0,
    "initialRebateExpiryDate": "00/00/0000",
    "initialRebatePeriod": 0,
    "initialUserFee1RebateIndicator": 0,
    "initialUserFee2RebateIndicator": 0,
    "initialUserFee3RebateIndicator": 0,
    "initialUserFee4RebateIndicator": 0,
    "initialUserFee5RebateIndicator": 0,
    "initialUserFee6RebateIndicator": 0
  },
  "insuranceDefermentDetails": {
    "insurancePeriod": 0,
    "insuranceStartDate": "00/00/0000",
    "insuranceTermIndicator": "0"
  },
  "interestDefermentDetails": {
    "interestPeriod": 0,
    "interestStartDate": "00/00/0000",
    "interestTermIndicator": "0"
  },
  "originalTerm": 3,
  "paymentDefermentDetails": {
    "paymentPeriod": 0,
    "paymentStartDate": "20/09/2021",
    "paymentTermIndicator": "0"
  },
  "planId": 70003,
  "productCode": "",
  "rebatePeriodIndicator": 0,
  "planSequenceNumber": 1,
  "secondRebateDetails": {
    "secondInsuranceRebateIndicator": 0,
    "secondInterestRebateIndicator": 0,
    "secondRebateExpiryDate": "00/00/0000",
    "secondRebatePeriod": 0,
    "secondUserFee1RebateIndicator": 0,
    "secondUserFee2RebateIndicator": 0,
    "secondUserFee3RebateIndicator": 0,
    "secondUserFee4RebateIndicator": 0,
    "secondUserFee5RebateIndicator": 0,
    "secondUserFee6RebateIndicator": 0
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
    "instance": "/v1/loans/0002000010000400044/originalDetails",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loans/{accountId}/originalDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|
| `planSequenceNumber` | Query Parameter | *integer*| 3 | Record number that identifies each Credit Plan Segment entity assigned to the account. The values are 0–999. The value 0 indicates a “phantom” plan used to disclose interest rates when no cash or retail plan exists for an account.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PS0004SF` | Get request - Record not Found |  

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
