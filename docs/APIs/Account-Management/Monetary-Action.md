# Monetary Action

This API is used to add or reverse finance input to an account based on action code and account Id given. This API updates the open-to-buy, memo debit and credit in real time on customer's account and generates an outstanding authorization record.

Fields that are not provided in the request object will be initialized to their default values. All numeric fields are initialized to zero and alphanumeric fields initialized to spaces.

## Endpoint

`POST /v1/accounts/monetaryAction`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json

{
  "businessUnit": 600,
  "accountId": "0006000011000000160",
  "actionCode": "AINQ",
  "transactionAmount": "3000.0",
  "effectiveDate": "18/08/2021",
  "departmentCode": " ",
  "skuNumber": 0,
  "salesClerk": " ",
  "paymentInstrumentId": "0006000011000000160",
  "ticketNumber": "0",
  "caseNumber": "0",
  "purchaseOrderNumber": "0",
  "planId": 10002,
  "storeNumber": 999999998,
  "authorizationCode": " ",
  "referenceNumber": "0",
  "actionCodePriority": "0",
  "insuranceCode": " ",
  "actionNotes": {
    "note1": " ",
    "note2": " ",
    "note3": " ",
    "note4": " ",
    "note5": " "
  },
  "representativeDetail": {
    "representativeId": "NAB",
    "referralOption": "0",
    "referralRepBusinessUnit": 0,
    "referralRepresentativeId": " "
  },
  "letterDetail": {
    "letterCode": " ",
    "letterBusinessUnit": 0
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000160",
  "paymentInstrumentId": "0006000011000000160",
  "decision": "A",
  "declineReason": " ",
  "notePurgeDate": "00/00/0000",
  "notesHistoryStatus": "O",
  "openToBuy": "-$80,072.00"
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
    "instance": "/v1/accounts/monetaryAction",
    "invalid-params": [
      "V5CR0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/accounts/monetaryAction).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `actionCode` | Payload | *string* | 4 | Action code placed on the account. |
| `transactionAmount` | Payload | *number* | 17 | Transaction amount to be posted. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Get Request - Record not found |
| `V8MA4001EA` | Rep activity model record not found on file |
| `V8MA4100EA` | Amt over limit and referral reps not available - use referral |
| `V8MA4001EB` | Org must be numeric and range from 001-998 |
| `V8MA4002EA` | Rep tally by org model record not on file |
| `V8MA4002EB` | ASM rep invalid must be grater than spaces |
| `V8MA4002EC` | Representative not found |
| `V8MA4003EA/V8MA4062EB` | maximum num of transaction reached for rep |
| `V8MA4003SA` | AMMA - action code not found |
| `V8MA4003SB` | AMMA - action code is  closed |
| `V8MA4003SC` | AMMA - action code is  purged |
| `V8MA4003SD` | AMMA - action code is  new |
| `V8MA4003SE` | AMMA - action code is add pending |
| `V8MA4004EA` | Invalid transaction type |
| `V8MA4004SV` | AMMA - invalid action type |
| `V8MA4061EA` | Account or card not found |
| `V8MA4061ES` | Account or card number required |
| `V8MA4005EC` | Invalid account status |
| `V8MA4006EA` | Monetary trans file issue in memo post routine |
| `V8MA4006EB` | ASM action code not on file |
| `V8MA4006EC` | Action code required |
| `V8MA4061ET` | System control file issue in memo post routine |
| `V8MA4061EU` | Base segment file issue in memo post routine |
| `V8MA4061EO` | Outstanding auth file issue in memo post routine |
| `V8MA4061EP` | Application issue try later |
| `V8MA4011EA/V8MA4012EM` | Effective date required |
| `V8MA4011EC/V8MA4012EC` | Invalid effective date |
| `V8MA4013ES` | Transaction amount must be numeric |
| `V8MA4012SA` | Transaction amount less than min initial load amount |
| `V8MA4013SM` | Referral not allowed - overlimit |
| `V8MA4013SP` | Transaction amount less than min initial load amount |
| `V8MA4012SB/V8MA4013SQ` | Transaction amount greater than max initial load amount |
| `V8MA4012SC/V8MA4013SR` | Transaction amount greater than max life time load amount |
| `V8MA4012ED/V8MA4013EM` | TRANSACTION AMOUNT REQUIRED |
| `V8MA4013EA/V8MA4014EM` | Plan number required |
| `V8MA4013EB/V8MA4014EN` | Plan number must equal the prepaid plan on acct |
| `V8MA4013EC/V8MA4036EN` | Plan not found on file |
| `V8MA4003ED` | Foreign use indicator invalid must be 0 or 1 |
| `V8MA4004SA` | Business unit must be numeric and range from 001-998 |
| `V8MA4017EA/V8MA4018EM` | Store number required |
| `V8MA4017EB/V8MA4036EO` | Store number not on file |
| `V8MA4012EC` | Transaction amount must be numeric and greater than zero |
| `V8MA4021EA/V8MA4029EG` | Priority must be numeric must be 0 to 3 |
| `V8MA4021SF` | Letter org must be numeric and less than 999 |
| `V8MA4022EA/V8MA4030EG` | Referal option must be valid 0, spaces or 1 |  
| `V8MA4023EA/V8MA4031EG` | Manual org must be numeric and 001-998 |
| `V8MA4024EA/V8MA4032EG` | Manual referal rep id was not supplied |  
| `V8MA4026EA/V8MA4001ED` | ASM not active  service usage not allowed  |
| `V8MA4027EA/V8MA4021EG` | Invalid letter code |
| `V8MA4028EA/V8MA4001EF` | Organization not found |
| `V8MA4029EA/V8MA4003EE/V8MA4030EA/V8MA4003EF` | Invalid foreign indicator |
| `V8MA4001ET` | Org not found |
| `V8MA4032EA` | Account or card not found |
| `V8MA4036EC` | Logo not found |
| `V8MA4033SA` | Case number must be numeric |
| `V8MA4033SB` | Case number must be greater than zero |
| `V8MA4001SA` | ASM org not found |
| `V8MA4034SA` | Not a valid wallet for load/reload |
| `V8MA4036EA` | ASM rep not allowed to access account org |
| `V8MA4043EA/V8MA4015EM` | Plan sequence is required |
| `V8MA4044EA/V8MA4016EM` | Dept is required |
| `V8MA4045EA/V8MA4017EM` | Auth code required |  
| `V8MA4048EA/V8MA4019EM` | Sku number required |
| `V8MA4049EA/V8MA4020EM` | Sales clerk required |
| `V8MA4050EA/V8MA4023EM` | Card number required |
| `V8MA4051EA/V8MA4024EM` | Card sequence required |
| `V8MA4052EA/V8MA4025EM` | Ticket number required |
| `V8MA4053EA/V8MA4026EM` | Purchase order number required |
| `V8MA4054EA/V8MA4027EM` | Reference number required |
| `V8MA4055EA/V8MA4028EM` | Insurance product required |
| `V8MA4056EA/V8MA4028EN` | Insurance product not appl for prepaid card |
| `V8MA4058EA` | Invalid ASM action code |
| `V8MA4059EA` | Tran code not found |
| `V8MA4060EA` | Invalid CMS tran code |  
| `V8MA4061EA` | Transaction not allowed for prepaid acct |
| `V8MA4062EA` | Transaction not valid for acct |
| `V8MA4063EA` | Manual referral org or rep not found |
| `V8MA4064EA` | Manual referal org not valid for this request |
| `V8MA4066EA` | Rep activity model record not found on file |  
| `V8MA4065EA` | Call to asxtap service failed |
| `V8MA4067EA` | Invalid effective date |
| `V8MA4068EA` | Transaction amount less than min initial load amount |
| `V8MA4069EA` | Transaction amt greater than max initial load amt |
| `V8MA4070EA` | Transaction amt greater than max life time load amt |
| `V8MA4071EA` | Reload not allowed on disposable card |
| `V8MA4072EA` | NBR of loads exceeded the max nbr of generic loads |
| `V8MA4073EA` | NBR of loads exceeded the max nbr of life time loads |
| `V8MA4074EA` | Exceeding the life time max load amount |
| `V8MA4075EA/V8MA4076EA/V8MA4077EA` | Exceeding the nbr limit for the frequency |
| `V8MA4078EA/V8MA4079EA/V8MA4080EA` | Exceeding the amount limit for the frequency |
| `V8MA4081EA/V8MA4082EA` | Transaction amount less than single load min amt |
| `V8MA4083EA` | Invalid fee occurrence number for prepaid txn |
| `V8MA4084EA/V8MA4085EA` | Invalid acct org real time fee process failure |
| `V8MA4086EA` | Invalid pct on the acct real time fee process failure |
| `V8MA4087EA` | Fee table not found on pct real time fee process failure |
| `V8MA4088EA` | Unknown error occurred in realtime fee process failure |
| `V8MA4089EA` | Amt over lmt and referral rep not avail, must manually refer actn |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
