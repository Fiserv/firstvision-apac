# Block Unblock Account

This service is used to update the Account Block Code.This service can be called with an account number. When either blockCode 1 or blockCode 2 has a value other than spaces, the new Block code can be applied to the unused entry on the account. This service is also used to remove block code from the account when space provided on existing block code field.

*If there is an entry in block code 1 or block code 2, the system is using the block code priorities defined at the logo record to decide to either apply the new block code values or to keep the existing block code value.
The system will check if the new block code 1 or 2 priority is greater than the existing block code priority then system will update the new block code value in block code 1 or block code 2 fields Other wise it will retain the existing value itself.* 
  
## Endpoint

`PUT /v1/accounts/{accountId}/blockUnblock`

## Payload Example

### Request Payload

```json
{
  "blockCode1": "X",
  "blockCode2": " "
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/blockUnblock).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `blockCode1/blockCode2` | Payload | *string* | 1 | Block Code to assign to the account. |


### Successful Response Payload

```json
{
  "accountId": "0001000010000510481",
  "blockCode1": "X",
  "blockCode1Date": "19/08/2021",
  "blockCode2": " ",
  "blockCode2Date": "19/08/2021",
  "businessUnit": 100
}

```

### Error Response Payload

```json
{
  "errorCode": "V5BS0125SV",
  "errorMessage": "Account - Invalid block code 1"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0011SF` | Update Request - Record add pending |
| `V5BS4001EA` | Invalid business unit |
| `V5BS4001SC` | Business unit is in purged status |
| `V5BS4002SA` | Invalid account number |  
| `V5BS0125SV` | Account - Invalid block code 1 |
| `V5BS0127SV` | Account - Invalid block code 2 |
| `V5BS0125SC` | Block Code 1 cannot be replaced with one of the lower priority |  
| `V5BS0127SC` | Block Code 2 cannot be replaced with one of the lower priority |