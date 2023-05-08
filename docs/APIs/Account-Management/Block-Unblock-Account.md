# Block Unblock Account

This API is used to update the Account Block Code. This service can be called with an account Id. When either block code 1 or block code 2 has a value other than spaces, the new block code can be applied to the unused entry on the account. This service is also used to remove block code from the account when space provided on existing block code field.

*If block code 1 or block code 2 is already applied on an account, system checks the block code priorities defined at the product to decide to either apply the new block code value or retain the existing block code value.
System will check if the new block code 1 or 2 priority is greater than the existing block code priority then system will update the new block code value in block code 1 or block code 2 fields Other wise it will retain the existing value itself. No block code priority check will occur when an unblock request is processed through this API.*
  
## Endpoint

`PUT /v1/accounts/{accountId}/blockUnblock`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "blockCode1": "X",
  "blockCode2": " "
}
```

<!--
type: tab
-->

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

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/accounts/0001000010000510481/blockUnblock",
    "invalid-params": [
      "V5BS0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/blockUnblock).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `blockCode1/blockCode2` | Payload | *string* | 1 | Block Code to assign to the account. |

### Error Codes

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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
