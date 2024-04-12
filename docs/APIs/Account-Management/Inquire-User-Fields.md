# Inquire User Fields

The API is used to fetch user fields at account level for a given account id.

## Endpoint

`GET /v1/accounts/{accountId}/userFields`

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
  "businessUnit": 200,
  "accountId": "0002000010000403266",
  "miscellaneousUserDetails": {
    "user01": "ABC",
    "user02": "A",
    "user03": "A1",
    "user04": "2738",
    "user05": "MOB",
    "user06": " ",
    "user07": " ",
    "user08": " ",
    "user09": " ",
    "user10": " ",
    "user11": " ",
    "user12": " "
  },
  "userDateDetails": {
    "date01": "10/01/2020",
    "date02": "21/02/2020",
    "date03": "00/00/0000",
    "date04": "00/00/0000",
    "date05": "00/00/0000",
    "date06": "00/00/0000",
    "date07": "00/00/0000",
    "date08": "00/00/0000",
    "date09": "00/00/0000",
    "date10": "00/00/0000",
    "date11": "00/00/0000",
    "date12": "00/00/0000",
    "date13": "00/00/0000",
    "date14": "00/00/0000"
  },
  "userCodeDetails": {
    "code01": "X1",
    "code02": "A",
    "code03": " ",
    "code04": " ",
    "code05": " ",
    "code06": "X1",
    "code07": "X1",
    "code08": "12",
    "code09": "AZ",
    "code10": " ",
    "code11": " ",
    "code12": " ",
    "code13": " ",
    "code14": "KY"
  },
  "userAmountDetails": {
    "amount01": "$900.00",
    "amount02": "$10000.00",
    "amount03": "$3840.00",
    "amount04": "$0.00",
    "amount05": "$0.00",
    "amount06": "$0.00",
    "amount07": "$0.00",
    "amount08": "$0.00",
    "amount09": "$10.00",
    "amount10": "$12.00",
    "amount11": "$123.00",
    "amount12": "$90.00",
    "amount13": "$66.00",
    "amount14": "$70.00"
  },
  "userApplicationDetails": {
    "user01": "RETAIL BNKING",
    "user02": "APPL2",
    "user03": "APPL3"
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
    "instance": "/v1/accounts/000200001000040329A/userFields",
    "invalid-params": [
      "V5BS0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/userFields).

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
