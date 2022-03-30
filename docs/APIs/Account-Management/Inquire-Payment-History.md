# Inquire Payment History

This API is used to retrive latest six payment details for given account number from FirstVision. Payment history feature in FirstVision is controlled by parameter, if feature is on, payment history will be retained otherwise no histrory will be retained. Although payment history is not retained, FirstVision retains delinquency paid fields in the Account Base Segment file.

## Endpoint

`GET /v1/accounts/{accountNumber}/paymentHistory`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Business Unit and Account Number should be sent as query parameters and path variable.***
 
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/paymentHistory).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the account. |

### Successful Response Payload

```json
{
  "accountNumber": "0006000011000000137",
  "businessUnit": 600,
  "paymentHistory": [
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$40.00",
      "cycleDue2DelinquencyPaidAmount": "$50.00",
      "cycleDue3DelinquencyPaidAmount": "$60.00",
      "cycleDue4DelinquencyPaidAmount": "$70.00",
      "cycleDue5DelinquencyPaidAmount": "$80.00",
      "cycleDue6DelinquencyPaidAmount": "$90.00",
      "cycleDue7DelinquencyPaidAmount": "$100.00",
      "cycleDue8DelinquencyPaidAmount": "$110.00",
      "cycleDue9DelinquencyPaidAmount": "$120.00",
      "originalPaymentAmount": "$40.00",
      "paymentAmount": "$10.00",
      "paymentDate": "18/08/2021",
      "prepaymentAmount": "$20.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$70.00"
    },
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$10.00",
      "cycleDue2DelinquencyPaidAmount": "$20.00",
      "cycleDue3DelinquencyPaidAmount": "$30.00",
      "cycleDue4DelinquencyPaidAmount": "$40.00",
      "cycleDue5DelinquencyPaidAmount": "$50.00",
      "cycleDue6DelinquencyPaidAmount": "$60.00",
      "cycleDue7DelinquencyPaidAmount": "$70.00",
      "cycleDue8DelinquencyPaidAmount": "$80.00",
      "cycleDue9DelinquencyPaidAmount": "$90.00",
      "originalPaymentAmount": "$10.00",
      "paymentAmount": "$10.00",
      "paymentDate": "19/08/2021",
      "prepaymentAmount": "$20.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$30.00"
    },
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$0.00"
    },
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$0.00"
    },
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$0.00"
    },
    {
      "cycleDue": 1,
      "cycleDue1DelinquencyPaidAmount": "$0.00",
      "cycleDue2DelinquencyPaidAmount": "$0.00",
      "cycleDue3DelinquencyPaidAmount": "$0.00",
      "cycleDue4DelinquencyPaidAmount": "$0.00",
      "cycleDue5DelinquencyPaidAmount": "$0.00",
      "cycleDue6DelinquencyPaidAmount": "$0.00",
      "cycleDue7DelinquencyPaidAmount": "$0.00",
      "cycleDue8DelinquencyPaidAmount": "$0.00",
      "cycleDue9DelinquencyPaidAmount": "$0.00",
      "originalPaymentAmount": "$0.00",
      "paymentAmount": "$0.00",
      "paymentDate": "00/00/0000",
      "prepaymentAmount": "$0.00",
      "reversalIndicator": "0",
      "totalDueBeforePayment": "$0.00"
    }
  ] 
}
```

### Error Response Payload

```json
{
   errorCode" :  V5PH0004SF" ,
   errorMessage" : Get Request - Record Not Found"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get Request - Record Not Found |