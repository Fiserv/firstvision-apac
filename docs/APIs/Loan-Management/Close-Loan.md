# Close Loan

This API is used to close a specific loan manually for a given account Id.

## Endpoint

`PUT /v1/loans/{accountId}/closeLoan`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "manualCloseIndicator": "3"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 200,
  "accountId": "0002000010000400044",
  "recordNumber": 1,
  "manualCloseIndicator": "3"
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
    "instance": "/v1/loans/0002000010000400044/closeLoan",
    "invalid-params": [
      "V5PS0004SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]

```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/loans/{accountId}/closeLoan).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account.|
| `recordNumber` | Query Parameter | *integer*| 3 | Record number that identifies each Credit Plan Segment record assigned to the account. The values are 0–999. The value 0 indicates a “phantom” plan used to disclose interest rates when no cash or retail plan exists for an account.|
| `manualCloseIndicator` | Payload | *string* | 1 | Field indicates the User wishes manually to cancel the Instalment Plan. Indicating the plan should be closed and will result in CMS generating transaction in the next batch run to credit the Instalment Plan and debit the rollover plan.|

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PS0004SF` | Get request - Record not Found |  
| `V5PS4411SA` | Account not present in ambs file |  
| `V5PS4411SB` | Amps - plan data record not found |
| `V5PS4410SB` | Org record not present |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
