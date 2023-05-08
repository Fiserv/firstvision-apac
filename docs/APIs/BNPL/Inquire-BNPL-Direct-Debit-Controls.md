# Inquire Direct Debit Controls

This API is used to fetch BNPL direct debit details for given account Id. It shows current parameter setup enabled for a given account Id used for direct debit processing.

## Endpoint

`GET /v1/bnpl/{accountId}/directDebitControls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account Id should be sent as path variable.***

<!--
type: tab
-->

```json
{
    "directDebitControls1": {
        "externalAccountType": "",
        "externalAccountId": "",
        "paymentStartDate": "00/00/0000",
        "paymentExpiryDate": "00/00/0000",
        "internationalBankingAccountId": "",
        "bankIdentifierCode": "",
        "paymentCardNumber": "0",
        "paymentCardNumberExpiryDate": 0,
        "repaymentType": 0,
        "paymentType": 0,
        "externalAccountsBankId": "",
        "routingBankId": "0"
    },
    "directDebitControls2": {
        "bankIdentifierCode": "",
        "paymentCardNumber": "0",
        "paymentCardNumberExpiryDate": 0,
        "internationalBankingAccountId": "",
        "routingBankId": "0",
        "externalAccountsBankId": "",
        "paymentExpiryDate": "00/00/0000",
        "externalAccountId": "",
        "paymentStartDate": "00/00/0000",
        "repaymentType": 0,
        "paymentType": 0,
        "externalAccountType": ""
    },
    "directDebitControls3": {
        "repaymentType": 0,
        "paymentType": 0,
        "externalAccountsBankId": "",
        "routingBankId": "0",
        "externalAccountType": "",
        "externalAccountId": "",
        "paymentStartDate": "00/00/0000",
        "paymentExpiryDate": "00/00/0000",
        "internationalBankingAccountId": "",
        "bankIdentifierCode": "",
        "paymentCardNumber": "0",
        "paymentCardNumberExpiryDate": 0
    },
    "directDebitControls4": {
        "repaymentType": 0,
        "paymentType": 0,
        "externalAccountsBankId": "",
        "externalAccountType": "",
        "externalAccountId": "",
        "paymentStartDate": "00/00/0000",
        "routingBankId": "0",
        "paymentExpiryDate": "00/00/0000",
        "internationalBankingAccountId": "",
        "bankIdentifierCode": "",
        "paymentCardNumber": "0",
        "paymentCardNumberExpiryDate": 0
    },
    "directDebitControls5": {
        "internationalBankingAccountId": "",
        "bankIdentifierCode": "",
        "paymentCardNumber": "0",
        "paymentStartDate": "00/00/0000",
        "paymentExpiryDate": "00/00/0000",
        "paymentCardNumberExpiryDate": 0,
        "repaymentType": 0,
        "paymentType": 0,
        "externalAccountsBankId": "",
        "routingBankId": "0",
        "externalAccountType": "",
        "externalAccountId": ""
    },
    "businessUnit": 700,
    "accountId": "0007000011253747002"
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
        "instance": "/v1/bnpl/0007000022427898801/directDebitControls",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5BS0004SF: Get Request - Record not found"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/bnpl/{accountId}/directDebitControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
