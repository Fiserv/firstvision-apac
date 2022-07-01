# Inquire Card Spend Limit Statistics

This service is used to fetch spend limit statistics for a given payment instrument identification.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/spendLimitStatistics`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Payment Instrument Identification should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/spendLimitStatistics).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |


### Successful Response Payload

```json
{
  "atmCashAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  },
  "businessUnit": 600,
  "otcCashAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  },
  "paymentInstrumentId": "0009544410000000047",
  "retailAuthorizationStatistics": {
    "ctdAuthorizationAmount": "$0.00",
    "ctdAuthorizationCount": 0,
    "ltdAuthorizationAmount": "$0.00",
    "ltdAuthorizationCount": 0,
    "todaysAuthorizationAmount": "$0.00",
    "todaysAuthorizationCount": 0,
    "ytdAuthorizationAmount": "$0.00",
    "ytdAuthorizationCount": 0
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED4001EN",
  "errorMessage": "Record purged or add pending "  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED4001EL` | Get request - Record not found |
|`V5ED4001EN` | Record purged or add pending |
|`V5ED4002EA` | Invalid card number |
|`V5ED4002ED` | Card number must be provided |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*
