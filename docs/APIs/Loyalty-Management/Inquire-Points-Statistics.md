# Inquire Points Statistics

This API is used to fetch points statistics for a given loyalty account

## Endpoint

`GET /v1/loyalty/{accountId}/statistics`

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
  "cycleToDateSpendAmount": "$1000.12",
  "yearToDateSpendAmount": "$12345.00",
  "cycleToDatePoints": {
    "bought": "100",
    "earned": "12",
    "bonus": "12",
    "redeemed": "12",
    "closed": "12",
    "expired": "12",
    "adjustIn": "12",
    "expiredInGracePeriod": "12",
    "adjustOut": "12",
    "total": "12"
  },
  "lifeToDatePoints": {
    "bought": "1000",
    "earned": "120",
    "bonus": "120",
    "redeemed": "120",
    "closed": "120",
    "expired": "120",
    "adjustIn": "120",
    "expiredInGracePeriod": "120",
    "adjustOut": "120",
    "total": "120"
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
    "errorCode": "442201",
    "instance": "/v1/loyalty/111111111111111112/details",
    "invalid-params": [
      "VKAI4002SA: INVALID ACCOUNT NUMBER"
    ],
    "source": "VPL",
    "status": 422,
    "title": "Unprocessable Entity"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/loyalty/{accountId}/statistics).

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
