# Update Pricing Control

This service is used update pricing control structure over an accounts. This service will update PCT Override, PCT Start Date, State Of Residency, State Of Issuance and PCT Expiry Date.

## Endpoint

`PUT /v1/accounts/{accountId}/pricingControls`

## Payload Example

### Request Payload

```json
{
  "issuanceId": "SX1",
  "residenceId": "SX1",
  "pctOverride": "HCS",
  "pctStartDate": "29/01/2022",
  "pctExpiryDate": "31/12/2025"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/pricingControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "accountId": "0006000011000000137",
  "businessUnit": 600,
  "issuanceId": "SX1",
  "pctExpiryDate": "31/12/2025",
  "pctOverride": "HCS",
  "pctStartDate": "29/01/2022",
  "residenceId": "SX1"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000131/pricingControls",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0302SB` | Issuance id not on usury table | 
| `V5BS0302SC` | Zero $$$$ in usury table for SOI | 
| `V5BS0302SD` | No pct rec found at this level | 
| `V5BS0302SE` | No active rates in processing control table | 
| `V5BS0302SF` | No file processing control table | 
| `V5BS0301SA` | Residence id not on usury table | 
| `V5BS0301SB` | Zero $$$ in usury table for SOR | 
| `V5BS0301SC` | Residence id can not be spaces | 
| `V5BS0301SD` | No pct rec found at this level | 
| `V5BS0301SE` | No active rates in processing control table | 
| `V5BS0301SF` | No file processing control table | 
| `V5BS0303SA` | No pct rec found at this level | 
| `V5BS0303SB` | No pct rec found at this level | 
| `V5BS0303SC` | No active rates in processing control table | 
| `V5BS0303SD` | No file processing control table | 
| `V5BS0304SA` | Pricing ctrl start/expiration dates conflict | 
| `V5BS0304SB` | Enter pricing ctrl when using dates | 
| `V5BS0304SC` | Start date less than the org next processing date | 
| `V5BS0304SD` | Expire date less than the org next processing date | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*