# List Insurance

This API is used to fetch the list of insurance products associated for a given account Id.

## Endpoint

`GET /v1/insurance/{accountId}/listInsurance`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
>***Account id should be sent as Path Variable.***  

<!--
type: tab
-->

```json
{
  "accountId": "0006000012000000085",
  "businessUnit": 600,
  "listOfInsuranceProducts": [
    {
      "Type": 0,
      "description": "DEFAULT INSURANCE TABLE",
      "insuranceId": "I1",
      "recordNumber": 1,
      "status": "F"
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
    "errorCode": "442201",
    "instance": "/v1/insurance/0006000012000000081/listInsurance",
    "invalid-params": [
      "V5I14002SD: NO INSURANCE PRODUCTS FOR THE ACCOUNT"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/insurance/{accountId}/listInsurance).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `customerId` | Path Variable | *string* | 19 | Unique identification number assigned to a customer. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5I14001SB` | No organization record on file or add pending |
| `V5I14002SD` | No insurance products for the account |
| `V5I14002SC` | No account on file or add pending |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
