# Update Accounts' Address ID

The service updates the address ID at account level upon successful validation of customer ID given in the request for a given Account ID.

## Endpoint

`PUT /v1/accounts/{accountId}/addressId`

## Payload Example

### Request Payload

```json
{
  "addressId": "HOME"
}
```

### Minimum	Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/addressId).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `customerId` | Query Variable | *string* | 19 | Unique identification number assigned to a customer. | 
| `addressId` | Payload | *string* | 15 | Address identifier to determine the type of address. Ex: Home, Office, etc. |


### Successful Response Payload

```json
{
  "businessUnit": "600",
  "accountId": "0004440010000000017",
  "addressId": "HOME",
  "customerId": "0000000001000000032"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0004440010000000017/addressId",
    "invalid-params": [
      "V5AU4002SC: ACCOUNT NUMBER NOT FOUND"
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
| `V5AU4002SA` | Account/Card number should not be spaces |
| `V5AU4002SC` | Account number not found |
| `V5AU4002SD` | AMBS record add pending |
| `V5AU4002SF` | AMBS record purged |
| `V5AU4002SG` | AMED record not found |
| `V5AU9910SA` | Address-ID should not be spaces |
| `V5AU9910SB` | Addr-ID should not have spacial chars, only - is allowed |
| `V5AU0102SA` | Invalid customer number |
| `V5AU4001SF` | Org not found |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*