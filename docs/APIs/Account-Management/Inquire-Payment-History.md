# Inquire Payment History

This API is used to retrive latest six payment details for given account number from FirstVision. Payment history feature in FirstVision is controlled by parameter, if feature is on, payment history will be retained otherwise no histrory will be retained. Although payment history is not retained, FirstVision retains delinquency paid fields in the Account Base Segment file.

## Endpoint

`GET /v1/accounts/{accountId}/paymentHistory`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json

{
  "accountId": "0006000011000000137",
  "businessUnit": 600,
  "paymentHistory": [
    {
      "beforePaymentTotalDueAmount": "$70.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$40.00",
      "cycleDue2DelinquencyPaidAmount": "$50.00",
      "cycleDue3DelinquencyPaidAmount": "$60.00",
      "cycleDue4DelinquencyPaidAmount": "$70.00",
      "cycleDue5DelinquencyPaidAmount": "$80.00",
      "cycleDue6DelinquencyPaidAmount": "$90.00",
      "cycleDue7DelinquencyPaidAmount": "$10.00",
      "cycleDue8DelinquencyPaidAmount": "$20.00",
      "cycleDue9DelinquencyPaidAmount": "$30.00",
      "originalPaymentAmount": "$40.00",
      "paymentAmount": "$10.00",
      "paymentDate": "18/08/2021",
      "prepaymentAmount": "$20.00",
      "reversalIndicator": "0"
    },
    {
      "beforePaymentTotalDueAmount": "$30.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$10.00",
      "cycleDue2DelinquencyPaidAmount": "$20.00",
      "cycleDue3DelinquencyPaidAmount": "$30.00",
      "cycleDue4DelinquencyPaidAmount": "$40.00",
      "cycleDue5DelinquencyPaidAmount": "$50.00",
      "cycleDue6DelinquencyPaidAmount": "$60.00",
      "cycleDue7DelinquencyPaidAmount": "$70.00",
      "cycleDue8DelinquencyPaidAmount": "$80.00",
      "cycleDue9DelinquencyPaidAmount": "$90.00",
      "originalPaymentAmount": "$10.00",
      "paymentAmount": "$10.00",
      "paymentDate": "19/08/2021",
      "prepaymentAmount": "$20.00",
      "reversalIndicator": "0"
    },
    {
      "beforePaymentTotalDueAmount": "$0.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0"
    },
    {
      "beforePaymentTotalDueAmount": "$0.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0"
    },
    {
      "beforePaymentTotalDueAmount": "$0.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0"
    },
    {
      "beforePaymentTotalDueAmount": "$0.00",
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0"
    }
  ]
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
    "instance": "/v1/accounts/0006000011000000190/paymentHistory",
    "invalid-params": [
      "V5PH0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/paymentHistory).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get request - Record Not Found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*