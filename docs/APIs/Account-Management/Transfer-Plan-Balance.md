# Transfer Plan Balance

This API is used to transfer the balance of a plan to a different plan within an account. This can be used for partial/full balance transfer and reversals.

## Endpoint

`POST /v1/accounts/transferPlanBalance`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 700,
  "accountId": "0007000011161782000",
  "transferType": "T",
  "transferFromPlanId": 5,
  "transferFromRecordNumber": 3,
  "transferToPlanId": 1,
  "transferToRecordNumber": 1,
  "amountFields": {
    "principalAmount": "0.00",
    "interestFeeAmount": "0.00",
    "insuranceFeeAmount": "0.00",
    "nsfFeeAmount": "0.00",
    "serviceFeeAmount": "0.00",
    "lateFeeAmount": "0.00",
    "membershipFeeAmount": "0.00",
    "overlimitFeeAmount": "0.00",
    "recoveryFeeAmount": "0.00",
    "collectionFeeAmount": "0.00",
    "userFee1Amount": "0.00",
    "userFee2Amount": "0.00",
    "userFee3Amount": "0.00",
    "userFee4Amount": "0.00",
    "userFee5Amount": "0.00",
    "userFee6Amount": "0.00"
  }
}
```

<!--
type: tab
-->

```json

{
  "businessUnit": 700,
  "accountId": "0007000011161782000",
  "transferFromPlanId": 5,
  "transferFromRecordNumber": 3,
  "transferToPlanId": 1,
  "transferToRecordNumber": 1,
  "amountFields": {
    "principalAmount": "$0.00",
    "interestFeeAmount": "$0.00",
    "insuranceFeeAmount": "$0.00",
    "nsfFeeAmount": "$0.00",
    "serviceFeeAmount": "$0.00",
    "lateFeeAmount": "$0.00",
    "membershipFeeAmount": "$0.00",
    "overlimitFeeAmount": "$0.00",
    "recoveryFeeAmount": "$0.00",
    "collectionFeeAmount": "$0.00",
    "userFee1Amount": "$0.00",
    "userFee2Amount": "$0.00",
    "userFee3Amount": "$0.00",
    "userFee4Amount": "$0.00",
    "userFee5Amount": "$0.00",
    "userFee6Amount": "$0.00"
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
    "instance": "/v1/accounts/transferPlanBalance",
    "invalid-params": [
      "V5XP4013EA: NO ORG RECORD ON FILE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/transferPlanBalance).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `transferFromPlanId` | Payload | *number* | 5 | Plan number associated with the credit plan segment from which to transfer funds. |  
| `transferFromRecordNumber` | Payload | *number* | 3 | Record number that identifies the credit plan segment on the account from which to transfer funds. |  
| `transferToPlanId` | Payload | *number* | 5 | Plan number to which you want to transfer the funds. |  
| `transferToRecordNumber` | Payload | *number* | 3 | Record number that identifies the credit plan segment on the account to which to transfer funds. |  

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5XP4013EA` | No org record on file |
| `V5XP4001EA` | Account number not found |
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
