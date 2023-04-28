# Inquire iPlans Details

This API is used to fetch iPlan details for a given account Id.

## Endpoint

`GET /v1/bnpl/{accountId}/iplanDetails`

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
  "businessUnit": 600,
  "productId": 0,
  "accountId": "0006000011000000103",
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
    "principalAmount": "$123.00",
    "interestAmount": "$5.00",
    "bookingFeeAmount": "$80.00",
    "snoozeFeeAmount": "$50.00",
    "missedPaymentFeeAmount": "$190.00",
    "totalAmount": "$1000.00",
    "snoozeFeeCount": 3,
    "missedPaymentFeeCount": 4
  },
  "interestRate": "0.00100%",
  "nextInstalmentPayDate": "01/07/2023",
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
      "totalAmount": "$1230.00",
      "payDate": "12/04/2023",
      "graceExpiryDate": "16/04/2023",
      "status": 1,
      "count": 24,
      "feeAmount": "$120.00"
    }
  ],
  "lastInstalmentDetails": {
    "instalmentPaymentDate": "10/05/2022",
    "instalmentPaymentAmount": "$10.00"
  },
  "lastSnoozeFeeDetails": {
    "snoozeFeeDate": "10/01/2022",
    "snoozeFeeAmount": "$10.00"
  },
  "lastMissedPaymentFeeDetails": {
    "missedPaymentFeeDate": "10/02/2022",
    "missedPaymentFeeAmount": "$10.00"
  },
  "24MonthsMissedPaymentProfileDetails": {
    "count01": 2,
    "count07": 2,
    "count13": 2,
    "count19": 2,
    "count02": 0,
    "count08": 0,
    "count14": 0,
    "count20": 0,
    "count03": 0,
    "count09": 0,
    "count15": 0,
    "count21": 0,
    "count04": 0,
    "count10": 0,
    "count16": 0,
    "count22": 0,
    "count05": 0,
    "count11": 0,
    "count17": 0,
    "count23": 0,
    "count06": 0,
    "count12": 0,
    "count18": 0,
    "count24": 0
  },
  "countDetails": {
    "missedPaymentCount": 1,
    "snoozeCount": 2,
    "switchCount": 2
  },
  "termDetails": {
    "initialTerm": 0,
    "currentTerm": 0,
    "remainingTerm": 0
  },
  "disclosedAmountDetails": {
    "principalAmount": "$200.00",
    "interestAmount": "$10.00",
    "bookingFeeAmount": "$12.00",
    "totalAmount": "$123.00"
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/bnpl/{accountId}/iplanDetails).

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
