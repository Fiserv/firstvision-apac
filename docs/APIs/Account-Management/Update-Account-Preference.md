# Update Account Preference

The service updates the statement preference, various customer IDs, address ID, source code, suppress token indicator for a given account ID. 

## Endpoint

`PUT /v1/accounts/{accountId}/preference`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json

{
  "statementPreferenceDetails": {
    "statementModeOrStatus": "O",
    "statementReprintAddressFlag": "C",
    "ownerCoOwnerStatementFlag": "0",
    "statementDeliveryMode": "E"
  },
  "customerId": "0000000001000000032",
  "correspondenceCustomerId": "0000000001000000065",
  "alternateCustomerIdDetails": {
    "customerIdFlag": "A",
    "customerId": "0000000001000000065",
    "customerIdExpiryDate": "15/04/2022",
    "customerIdEffectiveDate": "14/01/2021"
  },
  "addressId": "HOME",
  "sourceCode": " ",
  "isSupressTokenEnabled": "0"
}
```


<!--
type: tab
-->

```json

{
  "accountId": "0004440010000000017",
  "addressId": "",
  "alternateCustomerIdDetails": {
    "customerId": "0000000001000000065",
    "customerIdEffectiveDate": "14/01/2021",
    "customerIdExpiryDate": "15/04/2022",
    "customerIdFlag": "A"
  },
  "businessUnit": 600,
  "correspondenceCustomerId": "0000000001000000065",
  "customerId": "0000000001000000032",
  "isSupressTokenEnabled": "0",
  "sourceCode": " ",
  "statementPreferenceDetails": {
    "ownerCoOwnerStatementFlag": "0",
    "statementDeliveryMode": "E",
    "statementModeOrStatus": "O",
    "statementReprintAddressFlag": "C"
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
    "errorCode": "440401",
    "instance": "/v1/accounts/0006000011000000178/preference",
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

### Minimum	Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/preference).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountid` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0102SA` | Customer number cannot be zeroes |
| `V5BS0102SB` | Generic customer not allowed |
| `V5BS0102SC` | No active customer on file |
| `V5BS0172SA` | Generic customer not allowed |
| `V5BS0172SB` | No active customer on file |
| `V5BS0172SC` | Cust nbr not in add complete status |
| `V5BS0111SA` | Valid entries are space, A, or B |
| `V5BS0111SD` | Both alt exp date and cust nbr required |
| `V5BS0112SA` | Alt cust expires date should be a future date |
| `V5BS0521SN` | Suppress token is not numeric |
| `V5BS0521SV` | Invalid suppress token |
| `V5BS0521SZ` | Update access not granted for suppress token |
| `V5BS0122SA` | Valid entries are 0 Thru 9, H, O, R, S, U, Or Z |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*