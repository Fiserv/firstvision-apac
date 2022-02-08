# Update Direct Debit

The Direct Debit Update message enables the user to update the Direct Debit information on an account. 
The information that can be updated includes:  bank account and routing data and various other associated fields. 
This service does not initiate the Direct Debit, it just provides a mechanism to update the Direct Debit related fields.
> *It is necessary to perform an inquiry using the Direct Debit/Credit inquiry message first, as this service requires all fields to be sent in the request, whether they have been changed or not. If a tag is sent in empty, it is presumed that the field is to be deleted.*

## Endpoint

`PUT /v1/accounts/{accountNumber}/directDebit`

## Payload Example

### Request Payload

```json
{
  "dDPaymentExpiryDate": "10/04/2024",
  "product": 0,
  "dDRoutingBankID": 123456,
  "fixedPaymentAmount": 1,
  "paymentRemittanceMethod": "0",
  "dDNominatedPaymentAmtorPercentage": 10,
  "billingAcctInd": 0,
  "dDAccountNumber": "1000000057",
  "dDPaymentStartDate": "09/04/2022",
  "dDAccountType": "D"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/directDebit).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. | 
| `paymentRemittanceMethod` | Payload | *number* | 1 | Payment Remittance Method. |
| `dDPaymentStartDate` | Payload | *string* | 10 | DD Payment Start Date. |
| `dDPaymentExpiryDate` | Payload | *string* | 10 | DD Payment Expiry Date. |

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000057",
  "billingAcctInd": "0",
  "businessUnit": "600",
  "dDAccountNumber": "1000000057",
  "dDAccountType": "D",
  "dDNominatedPaymentAmtorPercentage": "10",
  "dDPaymentExpiryDate": "10/04/2024",
  "dDPaymentStartDate": "09/04/2022",
  "dDRoutingBankID": "123456",
  "fixedPaymentAmount": "1",
  "paymentRemittanceMethod": "0",
  "product": "600"
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

