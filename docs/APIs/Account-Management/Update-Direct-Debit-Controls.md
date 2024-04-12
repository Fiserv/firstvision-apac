# Update Direct Debit Controls

This API is used to update direct debit details for given account Id. This API does not initiate the direct debit, it just provides a mechanism to update the direct debit processing fields.

## Endpoint

`PUT /v1/accounts/{accountId}/directDebitControls`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "directDebitDetails": {
    "paymentRemittanceMethod": 2,
    "paymentStartDate": "04/10/2021",
    "paymentExpiryDate": "04/11/2022",
    "routingBankID": "123456",
    "accountType": "D",
    "externalAccountId": "1000000057",
    "nominatedType": 1,
    "nominatedPaymentAmountOrPercentage": "$10.00",
    "paymentType": 1,
    "paymentChangeDate": "04/10/2025",
    "customerName": "Alex Rey",
    "suspenseStartDate": "00/00/0000",
    "suspenseEndDate": "31/12/2999",
    "requestDays": 3
  }
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 600,
  "accountId": "0006000011000000103",
  "directDebitDetails": {
    "paymentRemittanceMethod": 2,
    "paymentStartDate": "04/10/2021",
    "paymentExpiryDate": "04/11/2022",
    "routingBankID": "123456",
    "accountType": "D",
    "externalAccountId": "1000000057",
    "nominatedType": 1,
    "nominatedPaymentAmountOrPercentage": "$10.00",
    "paymentType": 1,
    "paymentChangeDate": "04/10/2025",
    "customerName": "Alex Rey",
    "suspenseStartDate": "00/00/0000",
    "suspenseEndDate": "31/12/2999",
    "requestDays": 3
  },
  "informationalMessage": "Direct debit changes will reflect from next cycle."
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
    "instance": "/v1/accounts/0006000011000000103/directDebitControls",
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

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/directDebitControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found|
| `V5BS0628EA` | Pay remit method valid values are 0 through 2 |
| `V5BS0628EB` | When cms logo is set to Y, allowed values are 0, 1 or 2 |
| `V5BS0628EC` | Pay remit method not editable when debit active at cms logo level |
| `V5BS0628SV` | Invalid pay remittance method |
| `V5BS0616EA` | DD start date must be equal or greater than today's date |
| `V5BS0616EB` | DD start date must be less than DD expire date |
| `V5BS0616EC` | DD pymt start date not editable when debit active at logo |
| `V5BS0616SD` | ACH start date is not zero |
| `V5BS0614EA` | Expiry date must be equal or greater than next processing date or zeros |
| `V5BS0614EB` | ACH pmt exp not editable when debit active at logo |
| `V5BS0614SB` | Date ACH payment expire is not zero |
| `V5BS0612EA` | ACH routing nbr not editable when debit active at logo |
| `V5BS0612EK` | DD routing bank id 1st byte should be equalto zero and the last 9 bytes must be> zeros
| `V5BS0612SA` | Payment ACH rt number is not zero |
| `V5BS0621EA` | ACH acct type not editable when debit active at logo |
| `V5BS0621SV` | Invalid payment ACH debit type |
| `V5BS0622EA` | DD account nbr required field |
| `V5BS0622EB` | ACH account nbr not editable when debit active at logo |
| `V5BS0622SC` | Payment ACH db number other than zero and spaces |
| `V5BS0626EA` | DD NOM IND mst b 1,2,3,8,9 and dd amt/pct greater than or equal to 0 for dd pmt to 2 or 7 |
| `V5BS0626EB` | DD nom ind not editable when debit active at logo |
| `V5BS0626SV` | Invalid nominated ACH amount pricing control table flag |
| `V5BS0627EA` | DD nominated payment amount/percent must be equal to zero when dd nom ind is 0 or 3 OR 8 |
| `V5BS0627EB` | DD nominated payment amount/percent must be greater than zero when DD nom ind is 1 or 2 or 9 |
| `V5BS0627EC` | DD nominated payment amount/percent must be less than 100% and not 0 when DD nom indicator is 2 or 9 |
| `V5BS0627EE` | Nominated ACH pct/amt not editable when debit active at logo |
| `V5BS0627SG` | ACH pct amount is not zero |
| `V5BS0624SV` | AMBS - Invalid payment ACH flag |
| `V5BS0624EA` | Valid entries are 0, 1, 2 & 7 |
| `V5BS0624EB` | Logo doesn't allow DD/DC processing |
| `V5BS0624EC` | DD/DC processing not allowed for this account |
| `V5BS0624EF` | DD expre DT mst b 0 or > next process DT to reinstate direct debit |
| `V5BS0624EG` | PMT REV CNTR mst be < X, PMT REV LMT on logo to reinstate dir dbt |
| `V5BS0624EH` | ACH R/T nbr required |
| `V5BS0626EC` | DD payment type should be set as 2, when DD nom ind is 8 |
| `V5BS0626ED` | DD nom ind mst be 0,1,2,3,8 OR 9 |
| `V5BS9417ED` | DD nom acct name not editable when debit active at logo |
| `V5BS9418ED` | DD suspense dates not editable when debit active at logo |
| `V5BS9417EE` | Acct name/suspense dates not editable when debit active at logo |
| `V5BS9417EA` | DD nom acct name not editable when dd payment is inactive  |
| `V5BS9418EA` | Suspense start date is less than date next process |
| `V5BS9419EA` | Suspense end date is less than start date |
| `V5BS9418EB` | Suspense start/end date must be zero when dd is not active |
| `V5BS4001IA` | Direct debit changes will reflect from next cycle |
| `V5BS0631EA` | 017Must be equal or greater than cms file date |
| `V5BS0631EB` | 048Change dt mst b >= start dt and < expire dt, unless a dt is 0 |
| `V5BS0631EC` | 048Change dt mst b >= start dt and < expire dt, unless a dt is 0 |
| `V5BS0631ED` | DD pmt change date not editable when debit active at logo |
| `V5BS0615EA` | 040Must be zero when logo dd payment flag is S or D |
| `V5BS0615EB` | 041Must be 1 through 31 when logo dd payment flag is P or R |
| `V5BS0615EC` | 024Request day should be between 00 and 31 |
| `V5BS0615ED` | Request lead day not editable when debit active at logo |
| `V5BS0624EP` | DD suspense is in place-DD update cannot be allowed |
| `V5BS0626EG` | DD set/update not allowed for this account |
| `V5BS0626EH` | DD is auto-cancelled, update not allowed on this account |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
