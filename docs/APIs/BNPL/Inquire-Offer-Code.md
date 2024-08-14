# Inquire Offer Code

This API is used to fetch offer code details for a given business unit, product Id and offer code.

## Endpoint

`GET /v1/bnpl/{productId}/offerCodeDetails`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Product Id should be sent as path variable and business unit, offer type, configuration template should be sent a query parameter.***

<!--
type: tab
-->

```json
{
    "repaymentDetails": {
        "frequency": 0,
        "frequencyCount": 7,
        "terms": 3
    },
    "firstPaymentDetails": {
        "indicator": 1,
        "daysCount": 5,
        "instalmentBiilingIndicator": 1
    },
    "bookingFeeDetails": {
        "amountOrPercentage": "0",
        "minimumAmount": "$0.00",
        "maximumAmount": "$0.00",
        "type": " "
    },
    "snoozeDetails": {
        "type": 0,
        "daysCount": 0,
        "occurance": 0
    },
    "productId": 0,
    "configurationTemplate": "BNPLVR15",
    "offerType": 10,
    "description": "BNPL-SINGLE",
    "configurationTemplateExpiryDate": "01/01/2030",
    "businessUnit": 700,
    "bundleAccumulationDaysCount": 0,
    "missedPaymentFeeOccurance": 0,
    "interestRate": "150000",
    "isRestructureEnabled": 0,
    "bnplType": 0
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
        "instance": "/v1/bnpl/0/offerCodeDetails",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5QT0004SF: Get Request - Record not found"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/bnpl/{productId}/offerCodeDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *integer* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Path Variable | *integer* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |
| `offerType` | Query Parameter | *integer* | 2 | Type which indicates offer details. |
| `configurationTemplate` | Query Parameter | *string* | 10 | BNPL configuration template, set of controls that govern how each unique iPlan (BNPL Instalment Plan) is billed, what the payment frequency is, what fees are supplied etc. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5QT0103SD` | Valid offer type is 10 |
| `V5QT0422SA` | BNPL configuration template should not be spaces |
| `V5QT0403EA` | Please provide valid future date |
| `V5QT0404EA` | Accum days should be 00 when BNPL type not = 1 |
| `V5QT0406EA` | Bill repmt freq cnt is required for BNPL conf template |
| `V5QT0407EA` | Bill repmt terms is required for BNPL conf template |
| `V5QT0408EA` | BNPL first pmt def is required when BNPL type is 1 |
| `V5QT0409EA` | Days should be 00 when first pmt def is 0 |
| `V5QT0410EA` | Int bill should be 0 when days is 0 |
| `V5QT0412EA` | Invalid value: valid values are 0 to 100% |
| `V5QT0413EA` | Invalid value: booking fee min cannot be greater than max value |
| `V5QT0414EA` | Invalid value: booking fee max cannot be less than min value |
| `V5QT0415EA` | BNPL functionality is not active on org level |
| `V5QT0416EA` | BNPL snooze type is required to setup BNPL snooze days |
| `V5QT0419EA` | BNPL int rate is required for BNPL conf template |
| `V5QT0101EA` | No organization record on file |
| `V5QT0004SF` | Get Request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
