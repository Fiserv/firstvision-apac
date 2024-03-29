# Inquire Direct Debit Controls

This API is used to fetch direct debit details for given account Id. It shows current parameter setup enabled for a given account Id used for direct debit processing.

## Endpoint

`GET /v1/accounts/{accountId}/directDebitControls`

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
  "businessUnit": 600,
  "accountId": "0006000011000000137",
  "paymentRemittanceMethod": 2,
  "paymentStartDate": "04/10/2021",
  "paymentExpiryDate": "04/11/2021",
  "routingBankID": "123456",
  "accountType": "D",
  "externalAccountId": "00000001000000057",
  "nominatedType": 1,
  "nominatedPaymentAmountOrPercentage": "$10.00",
  "paymentType": 1,
  "paymentChangeDate": "04/10/2025",
  "customerName": "Alex Rey",
  "suspenseStartDate": "00/00/0000",
  "suspenseEndDate": "31/12/2999",
  "requestDays": 3
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
    "instance": "/v1/accounts/0006000011000000139/directDebitControls",
    "invalid-params": [
      "V5BS0010SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/directDebitControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
