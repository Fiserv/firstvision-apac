# Transfer Plan Balance

This service transfers the balance of a credit plan segment to a different credit plan segment within an account. With a plan transfer, you can transfer the entire balance of a credit plan segment.

## Endpoint

`POST /v1/accounts/transferPlanBalance`

## Payload Example

### Request Payload

```json

{
  "businessUnit": 200,
  "accountId": "0002000010000066752",
  "transferFromPlanId": 10002,
  "transferFromRecordNumber": 1,
  "transferToPlanId": 10001,
  "transferToRecordNumber": 0
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/transferPlanBalance).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 3 | Unique identification number associated with the organization. Valid values from 001-998. |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `transferToAccountId` | Payload | *number* | 5 | Plan number associated with the credit plan segment from which to transfer funds. |  
| `transferFromRecordNumber` | Payload | *number* | 3 | Record number that identifies the credit plan segment on the account from which to transfer funds. |  
| `transferToPlanId` | Payload | *number* | 5 | Plan number to which you want to transfer the funds. |  
| `transferToRecordNumber` | Payload | *number* | 3 | Record number that identifies the credit plan segment on the account to which to transfer funds. |  

### Successful Response Payload

```json

{
  "businessUnit": 200,
  "accountId": "0002000010000066752",
  "transferToPlanId": 10001,
  "transferToRecordNumber": 0
}
```

### Error Response Payload

```json
{
  "errorCode": "V5X24017SC",
  "errorMessage": "Transfer/Copy to account must not be on file for this"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5X24017SA` | Transfer/Copy to account number invalid |
| `V5X24017SC` | Transfer/Copy to account must not be on file for this |
| `V5X24018SA` | Transfer/Copy to logo invalid |
| `V5X24021SB` | Effective date invalid |
| `V5X24021SC` | Effective date greater than next processing date |
| `V5X24023EA` | Hcs parameters not applicable for non hcs account |
| `V5X24023EB` | Hcs parameters not applicable for this transfer |
| `V5X24025SA` | Invalid new card technology |
| `V5X24025SB` | Smart card not valid with card scheme 2 |
| `V5X24025SC` | Mobile smart contactless not valid with card scheme 2 |
| `V5X24025SC` | Product transfer must not transfer to logo of different cs 2 |
| `V5X24025SD` | Product transfer must not xfr to logo of diff card tech scheme 2 |
| `V5X24027SA` | Valid process type values are space, 0 or 1 |
| `V5X24027SB` | Mobile pi provisioning is not possible through sdp |
| `V5X24027SC` | Sdp process in progress. new sdp request not allowed |
| `V5X24027EE` | Logo does not support sdp requests |
| `V5X24030SA` | Transfer/copy to a logo with different card asso not allowed |
| `V5X24030SC` | Product transfer must not cross organizations |
| `V5X24030SG` | Cannot transfer account with pending card tech change |
| `V5X24030SJ` | Invalid new card technology |
| `V5X24030SK` | Too many embossers for accounts new |
| `V5X24030SL` | Account transfer not allowed due to pending card action |
| `V5X24030SM` | New card #s are about to be generated,enter 0 to continue |
| `V5X24030SD` | Product transfer must cross logos |
| `V5X24033SA` | Customer record already on file for this org |
| `V5X24033SB` | Customer record not on file in this org |
| `V5X24033SD` | Customer record must be active in this org |
| `V5X24033SH` | Generic customer not allowed |
| `V5X24034SD` | Customer record must be active in the dual org |
| `V5X24034SH` | Generic customer not allowed |
| `V5X24035SB` | Determined organization not equal transfer/copy from org |
| `V5X24035SC` | Determined logo not equal xfr/copy from logo for billing acct |
| `V5X24035SD` | Transfer to logo does not allow smart card-acct not transferred |
| `V5X24035SG` | Please review smart card embosser detail record on embosser record |