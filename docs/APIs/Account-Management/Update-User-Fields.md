# Update User Fields

The API is used to update user fields at account level for a given account id.

## Endpoint

`PUT /v1/accounts/{accountId}/userFields`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "miscellaneousUserDetails": {
    "user01": "ABC",
    "user02": "A",
    "user03": " ",
    "user04": " ",
    "user05": " ",
    "user06": " ",
    "user07": " ",
    "user08": " ",
    "user09": " ",
    "user10": " ",
    "user11": " ",
    "user12": " "
  },
  "userCodeDetails": {
    "code01": "X1",
    "code02": "A",
    "code03": " ",
    "code04": "AB",
    "code05": " ",
    "code06": " ",
    "code07": " ",
    "code08": " ",
    "code09": " ",
    "code10": "KY",
    "code11": "12",
    "code12": "X1",
    "code13": " ",
    "code14": " "
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
  "userAmountDetails": {
    "amount01": "10.00",
    "amount02": "10.00",
    "amount03": "10.00",
    "amount04": "10.00",
    "amount05": "100.00",
    "amount06": "123.00",
    "amount07": "10.00",
    "amount08": "10.00",
    "amount09": "10.00",
    "amount10": "10.00",
    "amount11": "10.00",
    "amount12": "0.00",
    "amount13": "1.00",
    "amount14": "10.00"
  },
  "userApplicationDetails": {
    "user01": "RETAIL BNKING",
    "user02": " ",
    "user03": " "
  }
}
```

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
    "user03": " ",
    "user04": " ",
    "user05": " ",
    "user06": " ",
    "user07": " ",
    "user08": " ",
    "user09": " ",
    "user10": " ",
    "user11": " ",
    "user12": " "
  },
  "userCodeDetails": {
    "code01": "X1",
    "code02": "A",
    "code03": " ",
    "code04": "AB",
    "code05": " ",
    "code06": " ",
    "code07": " ",
    "code08": " ",
    "code09": " ",
    "code10": "KY",
    "code11": "12",
    "code12": "X1",
    "code13": " ",
    "code14": " "
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
  "userAmountDetails": {
    "amount01": "$10.00",
    "amount02": "$10.00",
    "amount03": "$10.00",
    "amount04": "$10.00",
    "amount05": "$100.00",
    "amount06": "$112.00",
    "amount07": "$10.00",
    "amount08": "$10.00",
    "amount09": "$10.00",
    "amount10": "$10.00",
    "amount11": "$10.00",
    "amount12": "$0.00",
    "amount13": "$1.00",
    "amount14": "$10.00"
  },
  "userApplicationDetails": {
    "user01": "RETAIL BNKING",
    "user02": " ",
    "user03": " "
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
    "instance": "/v1/accounts/0006000011000000111/userFields",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/userFields).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update request - Record not found |
| `V5BS0121SA` | Valid entries are 01 Thru 31 |
| `V5BS4001SG` | Org record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
