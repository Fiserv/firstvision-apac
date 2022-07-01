# Update Issue Reissue Delivery Option

This service is used to update the issue and re-issue delivery options on Payment Card Number.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/issueReissueDeliveryOption`

## Payload Example

### Request Payload

```json
{
  "issueDeliveryOption": "1",
  "reissueDeliveryOption": "5"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/issueReissueDeliveryOption).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "issueDeliveryOption": "1",
  "paymentInstrumentId": "0009544410000000047",
  "reissueDeliveryOption": "5"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0330SV",
  "errorMessage": "Card - invalid  reissue-deliv-option"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0330SV` | Card - invalid  reissue-deliv-option |        
| `V5ED0331SV` | Card - invalid  issue-deliv-option | 
| `V5ED0010SF` | Update request - Record not found |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).* 



