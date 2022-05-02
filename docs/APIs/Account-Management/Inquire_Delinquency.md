# Inquire Delinquency

 This service provides delinquency details for a given account number like 30 to 150 day delinquent amount, last deliquent date, current cycle due etc.

## Endpoint

`GET /v1/accounts/{accountNumber}/deliquencyDetails`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/deliquencyDetails).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account. | 

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000509",
  "businessUnit": 600,
  "delinquencyDetailsRes": {
    "120daysDelinquentAmount": "$0.00",
    "150daysDelinquentAmount": "$0.00",
    "180daysDelinquentAmount": "$0.00",
    "210daysDelinquentAmount": "$0.00",
    "30daysDelinquentAmount": "$0.00",
    "60daysDelinquentAmount": "$0.00",
    "90daysDelinquentAmount": "$0.00",
    "currentDue": "$0.00",
    "cycleDue": "0",
    "lastDeliquentDate": "00/00/0000",
    "pastDuePaymentAmount": "$0.00",
    "paymentDaysDeliquent": 0,
    "previousCycleDue": 0
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0004SF",
  "errorMessage": "Get Request - Record Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0004SF` | Get Request - Record Not Found |