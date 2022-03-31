# Update Accounts' Direct Debit

The Direct Debit Update message enables the user to update the Direct Debit information on an account. The information that can be updated includes: bank account and routing data and various other associated fields. This service does not initiate the Direct Debit, it just provides a mechanism to update the Direct Debit related fields.

## Endpoint

`PUT /v1/accounts/{accountNumber}/directDebit`

## Payload Example

### Request Payload

```json
{
  "directDebitDetailsReq": {
    "paymentRemittanceMethod": "0",
    "ddPaymentStartDate": "04/10/2021",
    "ddPaymentExpiryDate": "04/11/2022",
    "ddRoutingBankId": "123456",
    "ddAccountType": "D",
    "ddAccountNumber": "1000000057",
    "fixedPaymentAmount": "1",
    "ddNominatedPaymentAmtOrPercentage": "10"
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/directDebit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique identification number of the Account. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
 "accountNumber": "0006000011000000103",
  "businessUnit": 600,
  "directDebitDetailsRes": {
    "ddAccountNumber": "1000000057",
    "ddAccountType": "D",
    "ddNominatedPaymentAmtOrPercentage": "10",
    "ddPaymentExpiryDate": "04/11/2022",
    "ddPaymentStartDate": "04/10/2021",
    "ddRoutingBankId": "123456",
    "fixedPaymentAmount": "1",
    "paymentRemittanceMethod": "0"
  }
}  
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0628SV",
  "errorMessage": " Invalid pay remittance method "
}
```

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
| `V5BS0614SB` | Date ach payment expire is not zero |
| `V5BS0612EA` | ACH routing nbr not editable when debit active at logo |
| `V5BS0612EK` | DD routing bank id 1st byte should be equalto zero and the last 9 bytes must be> zeros
| `V5BS0612SA` | Payment ach rt number is not zero |
| `V5BS0621EA` | ACH acct type not editable when debit active at logo |
| `V5BS0621SV` | Invalid payment ach debit type |
| `V5BS0622EA` | DD account nbr required field |
| `V5BS0622EB` | ACH account nbr not editable when debit active at logo |
| `V5BS0622SC` | Payment ach db number other than zero and spaces |
| `V5BS0626EA` | DD nom ind mst b 1,2,3,9 and DD amt/pct greater than or equal to 0 for DD pmt to 2 or 7 |
| `V5BS0626EB` | DD nom ind not editable when debit active at logo |
| `V5BS0626SV` | Invalid nominated ach amount pricing control table flag |
| `V5BS0627EA` | DD nominated payment amount/percent must be equal to zero when DD nom ind is 0 or 3 |
| `V5BS0627EB` | DD nominated payment amount/percent must be greater than zero when DD nom ind is 1 or 2 or 9 |
| `V5BS0627EC` | DD nominated payment amount/percent must be less than 100% and not 0 when DD nom indicator is 2 or 9 |
| `V5BS0627EE` | Nominated ach pct/amt not editable when debit active at logo |
| `V5BS0627SG` | ACH pct amount is not zero |