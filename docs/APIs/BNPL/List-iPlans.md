# List iPlans

This API is used to fetch the list of iPlans associated for a given account Id.

## Endpoint

`GET /v1/bnpl/{accountId}/listIplans`

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
  "listIplans": [
    {
      "type": "TXN",
      "status": 1,
      "openDate": "01/14/2021",
      "currentBalance": "$101.00",
      "totalDueAmount": "$200.00",
      "configurationTemplateDescription": "Config template10",
      "configurationTemplate": "TMPL1",
      "sequenceNumber": 2
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
        "errorCode": "240009",
        "detail": "Please refer to invalid-params for error details",
        "title": "Required fields missing",
        "instance": "/v1/bnpl/0007000011253747002/listIplans",
        "source": "APT",
        "status": 400,
        "invalid-params": [
            "V5IP4002EA: ACCOUNT NUMBER NOT FOUND OR IN INVALID STATUS"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/bnpl/{accountId}/listIplans).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5IP4001EA` | Org is in add pending |
| `V5IP4002EA` | Account number not found or in invalid status |
| `V5IP4002EB` | Acct level bnpl sequence number is zero/acct not found,transferred |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
