# Inquire Spend Limits 

This service is used to inquire	 the spending limits to control the card usage. These limits are set to individual card level like maximum ATM, OTC, Retail etc authorizatoin amount and count.

## Endpoint

`GET /v1/cards/{paymentInstrumentId}/spendLimits`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Payment Instrument Identification should be sent as path variable..***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{paymentInstrumentId}/spendLimits).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |

### Successful Response Payload

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010434272",
  "spendLimitControls": {
    "maximumAtmCashAuthorizationsAmount": "$100.00",
    "maximumAtmCashAuthorizationsCount": 1,
    "maximumAuthorizationsFrequency": "1",
    "maximumOtcAuthorizationsCount": 1,
    "maximumOtcCashAuthorizationsAmount": "$200.00",
    "maximumRetailAuthorizationsAmount": "$100.00",
    "maximumRetailAuthorizationsCount": 1,
    "maximumSingleAtmTransactionAmount": "$100.00",
    "maximumSingleOtcCashAuthorizationAmount": "$100.00",
    "maximumSingleRetailAuthorizationAmount": "$0.00"
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0004SF",
  "errorMessage": "Update request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5ED0004SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*

