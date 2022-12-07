# Inquire Authorization Details

This service is used to provide Authorization detail of transaction when internal reference number provided in input request. 
This service called immediately after Auth Request service and it will provide authorization details of the transaction. 
*Kindly use List Outstanding Authorization API to fetch detail of transaction when daily batch is completed or next day when transaction is not available in FAS log file.*

## Endpoint

`GET /v1/auth/{internalReferenceNumber}/authDetails`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Internal Reference Number should be sent as query parameter.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/auth/{internalReferenceNumber}/authDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `internalReferenceNumber` | Path Variable | *string* | 9 | This field indicate the internal reference number of the authorizatoin transaction.| 

### Successful Response Payload

```json
{
  "accountDetails": {
    "accountOpenDate": "01/05/2021",
    "cardFeeDate": "00/00/0000",
    "chargeOffDate": "00/00/0000",
    "chargeOffReason": "",
    "chargeOffStatus": "0",
    "creditClassification": "N1",
    "creditLimitOverlimitPercentage": "$1.00",
    "customerid": "0001000000000150191",
    "delinquentPaymentDaysCount": "000",
    "lastDelinquentDate": "00/00/0000",
    "lastPaymentAmount": "$0.00",
    "lastPaymentDate": "00/00/0000",
    "lastPurchaseAmount": "$0.00",
    "lastPurchaseDate": "00/00/0000",
    "lastReturnCheckCount": 0,
    "lastReturnCheckDate": "00/00/0000",
    "lastStatementDate": "30/04/2021"
  },
  "accountStatus": "A",
  "action": "A",
  "authorizationCode": "055358",
  "availableCredit": "$8,946.36",
  "blockAndWarningCodeDetails": {
    "blockCode1": "",
    "blockCode1Date": "00/00/0000",
    "blockCode2": "",
    "blockCode2Date": "00/00/0000",
    "warningCode": "0000000"
  },
  "collectionDetails": {
    "collectionDate": "00/00/0000",
    "collectionReason": 0
  },
  "creditLimit": "$0.00",
  "currentBalance": "$0.00",
  "currentCycleDue": 0,
  "delinquentDaysCount": 0,
  "disputedAmount": "$0.00",
  "disputedItemCount": 0,
  "expiryDate": "30/04/2024",
  "maskedPaymentCardNumber": "000404940XXXXXX5286",
  "uniqueTransactionId": "APP179777002220113443300011123456111",
  "memoDetails": {
    "memoCreditAmount": "$0.00",
    "memoCreditCount": 0,
    "memoDebitAmount": "$549.58",
    "memoDebitCount": 134
  },
  "merchantDetails": {
    "merchantBusinessUnit": "100",
    "merchantCategoryCode": "05999",
    "merchantId": "999999998"
  },
  "planId": "10001",
  "reason": "APPROVED",
  "responseCode": "00",
  "temporaryCreditLimit": "$0.00",
  "totalDueAmount": "$0.00",
  "transactionAmount": "2.00"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/auth/3839405/authDetails",
    "invalid-params": [
      "V7RS0004SF: FMLG - RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V7RS0004SF` | FMLG - record not found |
| `V7RQ4001SA` | Auth system record not initialized |
| `V7RQ4001SB` | End-of-day cutoff being processed | 
| `V7RQ4001SC` | After hours update in progress |
| `V7RQ4001EE` | Country code not valid in cms org rec for merch |


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
