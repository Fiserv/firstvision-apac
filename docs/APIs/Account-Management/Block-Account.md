# Block-Unblock Account

This service is used to update the Account Block Code.This service can be called with an account number. When either blockCode 1 or blockCode 2 has a value other than spaces, the new Block code can be applied to the unused entry on the account. This service is also used to remove block code from the account when space provided on existing block code field.

*If there is an entry in block code 1 or block code 2, the system is using the block code priorities defined at the logo record to decide to either apply the new block code values or to keep the existing block code value.
The system will check if the new block code 1 or 2 priority is greater than the existing block code priority then system will update the new block code value in block code 1 or block code 2 fields Other wise it will retain the existing value itself.* 
  
## Endpoint

`PUT /v1/accounts/{accountNumber}/blockUnblock`

## Payload Example

### Request Payload

```json
{
  "blockCode1": "X",
  "blockCode2": " "
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/blockUnblock).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `blockCode1/blockCode2` | Payload | *string* | 1 | Block Code to assign to the account. |

### Successful Response Payload

```json
{
  "accountNumber": "0001000010000510481",
  "billingAcctInd": "0",
  "blockCode1": "X",
  "blockCode2": " ",
  "blockCodeDate1": "19/08/2021",
  "blockCodeDate2": "19/08/2021",
  "businessUnit": "100",
  "product": "1"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0125SV",
  "errorMessage": "Account - Invalid Block Code 1"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record Not Found |
| `V5BS0011SF` | Update Request - Record Add Pending |
| `V5BS4001EA` | Invalid Business Unit |
| `V5BS4001SC` | Business Unit is in Purged Status |
| `V5BS4002SA` | Invalid Account Number |  
| `V5BS0125SV` | Account - Invalid Block Code 1 |
| `V5BS0127SV` | Account - Invalid Block Code 2 |
| `V5BS0125SC` | Block Code 1 cannot be replaced with one of the lower priority |  
| `V5BS0127SC` | Block Code 2 cannot be replaced with one of the lower priority |
