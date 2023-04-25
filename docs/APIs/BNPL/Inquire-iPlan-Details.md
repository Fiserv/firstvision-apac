# Inquire iPlans Details

This API is used to fetch iPlan details for a given account Id.

## Endpoint

`GET /v1/accounts/{accountId}/iplanDetails`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable and sequence number should be sent as query parameter.***

<!--
type: tab
-->

```json
{
  "businessUnit": 700,
  "productId": 0,
  "accountId": "0007000011000000103",
  "configurationTemplate": "TMPL1",
  "sequenceNumber": 2,
  "status": 1,
  "previousStatus": 1,
  "type": "TXN",
  "iplanDesc": "Bajaj Electronics",
  "bundleStartDate": "10/01/2023",
  "bundleEndDate": "10/12/2025",
  "firstInstalmentAmount": "$100.00",
  "firstInstalmentDate": "01/02/2023",
  "finalInstalmentAmount": "$100.00",
  "finalInstalmentDate": "01/02/2025",
  "fixedInstalmentAmount": "$100.00",
  "currentBalance": "$101.00",
  "totalDueAmount": "$200.00",
  "billedNotPaidDetails": {
    "principalAmount": "$1230.00",
    "unbilledPrincipalAmount": "$12300.00",
    "interestAmount": "$1200.00",
    "bookingFeeAmount": "$100.00",
    "snoozeFeeAmount": "$100.00",
    "missedPaymentFeeAmount": "$100.00"
  },
  "billedAmountDetails": {
    "billedPrincipalAmount": "$123.00",
    "billedInterestAmount": "#5.00",
    "billedBookingFeeAmount": "$80.00",
    "billedSnoozeFeeAmount": "$50.00",
    "billedMissedPaymentFeeAmount": "$190.00",
    "billedTotalAmount": "$1000.00",
    "billedSnoozeFeeCount": 3,
    "billedMissedPaymentFeeCount": 4
  },
  "interestRate": "000020.00%",
  "nextInstalmentPayDate": "01/7/2023",
  "switchHistoryDetails": [
    {
      "configurationTemplateBeforeSwitch": "TMPL20",
      "switchRequestedDate": "01/01/2023"
    }
  ],
  "instalmentScheduleDetails": [
    {
      "principalAmount": "$10000.00",
      "interestAmount": "$120.00",
      "bookingFeeAmount": "$200.00",
      "snoozeFeeAmount": "$300.00",
      "missedPaymentAmount": "$120.00",
      "TotalAmount": "$1230.00",
      "payDate": "12/04/2023",
      "graceExpiryDate": "16/04/2023",
      "status": 1,
      "count": 24,
      "feeAmount": "$120.00"
    }
  ],
  "lastInstalmentDetails": {
    "lastSnoozeFeeDate": "10/01/2022",
    "lastInstalmentPaymentAmount": "$10.00"
  },
  "lastSnoozeFeeDetails": {
    "lastSnoozeFeeAmount": "$10.00"
  },
  "lastMissedPaymentFeeDetails": {
    "lastMissedPaymentFeeDate": "10/02/2022",
    "lastMissedPaymentFeeAmount": "$10.00"
  },
  "24MonthMissedPaymentProfileDetails": {
    "missedPaymentCount01": 2,
    "missedPaymentCount07": 2,
    "missedPaymentCount13": 2,
    "missedPaymentCount19": 2,
    "missedPaymentCount02": 0,
    "missedPaymentCount08": 0,
    "missedPaymentCount14": 0,
    "missedPaymentCount20": 0,
    "missedPaymentCount03": 0,
    "missedPaymentCount09": 0,
    "missedPaymentCount15": 0,
    "missedPaymentCount21": 0,
    "missedPaymentCount04": 0,
    "missedPaymentCount10": 0,
    "missedPaymentCount16": 0,
    "missedPaymentCount22": 0,
    "missedPaymentCount05": 0,
    "missedPaymentCount11": 0,
    "missedPaymentCount17": 0,
    "missedPaymentCount23": 0,
    "missedPaymentCount06": 0,
    "missedPaymentCount12": 0,
    "missedPaymentCount18": 0,
    "missedPaymentCount24": 0
  },
  "countDetails": {
    "missedPmtCount": 1,
    "snoozeCount": 2,
    "switchCount": 2
  },
  "termDetails": {
    "initialTerm": 0,
    "currentTerm": 0,
    "remainingTerm": 0
  },
  "disclosedAmountDetails": {
    "disclosedPrincipalAmount": "$200.00",
    "disclosedInterestAmount": "$10.00",
    "disclosedBookingFeeAmount": "$12.00",
    "disclosedTotalAmount": "#123.00"
  }
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/bnpl/0007000011000000103/iplanDetails",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V52P9981SF: RECORD NOT FOUND"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/iplanDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `sequenceNumber` | Query Parameter | *integer* | 5 | This is the iPlan sequence number when each time a new iPlan is created |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V52P9981SF` | Record Not Found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
