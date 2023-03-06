# Inquire Points Account

This API is used to fetch points account details.

## Endpoint

`GET /v1/loyalty/{accountId}/details`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable and schemeId, businessUnit should be sent as query parameters.***

<!--
type: tab
-->

```json
{
  "schemaName": "REWARDS",
  "status": 1,
  "businessUnit": 600,
  "accountId": "1111111111111111111",
  "schemaId": "10101",
  "typeOfCustomer": "I",
  "totalAmount": "$100.00",
  "totalAvailablePoints": "1000",
  "cashValue": "$50.00",
  "enrollmentChannel": "NETB",
  "lastStatusChangeDate": "12/01/2021"
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
    "instance": "/v1/loyalty/1111111111111111111/details",
    "invalid-params": [
      "VKAI4006SA: POINTS SCHEME RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loyalty/{accountId}/details).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number that identifies the points account. |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `schemeId` | Query Parameter | *number* | 5 | Unique identification number of the points scheme associated with the organization. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VKAI4001SF` | Invalid Org |
| `VKAI4002SA` | Invalid Account Number |
| `VKAI4003SA` | Organization record is in pending add status |
| `VKAI4004SA` | Organization record is incomplete/closed/purged |
| `VKAI4005SA` | Organization record not found |
| `VKAI4006SA` | Points scheme record not found |
| `VKAI4007SA` | Points scheme record is in pending add status |
| `VKAI4008SA` | Points scheme record is incomplete/closed/purged |
| `VKAI4009SA` | Invalid scheme date range |
| `VKAI4010SA` | Points account record not found |
| `VKAI4011SA` | Points account record is incomplete/closed/pending purge/purged |
| `VKAI4012SA` | Points account record is in pending add status |
| `VKAI4013SA` | Account demographic record not found |
| `VKAI4014SA` | Account demographic record status is incomplete |
| `VKAI4015SA` | Account demographic record is in pending add status |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
