# List Transactions

This service provides the list of various transactions like memo, outstanding, unbilled and billed with in a given a date range. 

## Endpoint

`GET /v1/accounts/{accountId}/listTransactions`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id, start date and end date should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/listTransactions).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 
| `startDate` | Query Parameter | *date* | 10 | Start date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. | 
| `endDate` | Query Parameter | *date* | 10 | End date for the transaction selection criteria, The format is MM/DD/YYYY or DD/MM/YYYY depending on the DATE FORMAT on System Control. |

### Successful Response Payload

```json

{
  "transactionList": [
    {
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "20210513",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "VT211330002000010000025",
      "transactionAmount": 1000,
      "transactionCode": 4000,
      "transactionType": "D"
    },
    {
      "description": "Australia Bank         Melbaourne    AU",
      "effectiveDate": "20210513",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "VT211330002000010000026",
      "transactionAmount": 100,
      "transactionCode": 4579,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210513",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210513",
      "referenceNumber": "19999999980513199980010",
      "transactionAmount": 1000,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "Wall Mart LLC AUS      Sydney        AU",
      "effectiveDate": "20210518",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210518",
      "referenceNumber": "VT211380004000010000001",
      "transactionAmount": 1501,
      "transactionCode": 4567,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210518",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210518",
      "referenceNumber": "19999999980518199980010",
      "transactionAmount": 1501,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "Wall Mart LLC          Sydney        AU",
      "effectiveDate": "20210519",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000010",
      "transactionAmount": 1111,
      "transactionCode": 4000,
      "transactionType": "D"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000064",
      "transactionAmount": 2500,
      "transactionCode": 6800,
      "transactionType": "D"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000065",
      "transactionAmount": 2100,
      "transactionCode": 6804,
      "transactionType": "D"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000066",
      "transactionAmount": 400,
      "transactionCode": 6806,
      "transactionType": "D"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000067",
      "transactionAmount": 1000,
      "transactionCode": 6804,
      "transactionType": "D"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000068",
      "transactionAmount": 500,
      "transactionCode": 6806,
      "transactionType": "D"
    },
    {
      "description": "Wall Mart LLC AUS      Sydney        AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000042",
      "transactionAmount": 1003,
      "transactionCode": 4004,
      "transactionType": "D"
    },
    {
      "description": "Australia Bank LLC     Sydney        AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000048",
      "transactionAmount": 1021,
      "transactionCode": 4545,
      "transactionType": "D"
    },
    {
      "description": "Australia Bank LLC     Sydney        AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000050",
      "transactionAmount": 1025,
      "transactionCode": 4561,
      "transactionType": "D"
    },
    {
      "description": "EDAF EFTPOS              PEASANT NEST AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000059",
      "transactionAmount": 2100,
      "transactionCode": 6816,
      "transactionType": "C"
    },
    {
      "description": "EDAF EFTPOS              PEASANT NEST AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000060",
      "transactionAmount": 2200,
      "transactionCode": 6816,
      "transactionType": "C"
    },
    {
      "description": "EDAF EFTPOS              PEASANT NEST AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000062",
      "transactionAmount": 2300,
      "transactionCode": 6818,
      "transactionType": "C"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000069",
      "transactionAmount": 1450,
      "transactionCode": 6805,
      "transactionType": "C"
    },
    {
      "description": "CHIP EFTPOS              PHEASANTS NESAU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000070",
      "transactionAmount": 50,
      "transactionCode": 6807,
      "transactionType": "C"
    },
    {
      "description": "Wall Mart LLC USA      Florida       US",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000029",
      "transactionAmount": 1005,
      "transactionCode": 4106,
      "transactionType": "C"
    },
    {
      "description": "Australia Bank LLC     Sydney        AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "VT211400002000010000041",
      "transactionAmount": 1024,
      "transactionCode": 4560,
      "transactionType": "C"
    },
    {
      "description": "EDAF EFTPOS              PEASANT NEST AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "ST211400003000010000063",
      "transactionAmount": 2300,
      "transactionCode": 6819,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210519",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210519",
      "referenceNumber": "19999999980520199980010",
      "transactionAmount": 1111,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980020",
      "transactionAmount": 2500,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980030",
      "transactionAmount": 2100,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980040",
      "transactionAmount": 400,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980050",
      "transactionAmount": 1000,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980060",
      "transactionAmount": 500,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980070",
      "transactionAmount": 1003,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980080",
      "transactionAmount": 1021,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980090",
      "transactionAmount": 1025,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10001,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980100",
      "transactionAmount": 2100,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "PRINCIPAL DEBIT ADJUSTMENT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980110",
      "transactionAmount": 1300,
      "transactionCode": 2701,
      "transactionType": "D"
    },
    {
      "description": "PRINCIPAL CREDIT ADJUSTMENT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10001,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980120",
      "transactionAmount": 1300,
      "transactionCode": 1701,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10001,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980130",
      "transactionAmount": 2200,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "PRINCIPAL DEBIT ADJUSTMENT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980140",
      "transactionAmount": 1400,
      "transactionCode": 2701,
      "transactionType": "D"
    },
    {
      "description": "PRINCIPAL CREDIT ADJUSTMENT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10001,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980150",
      "transactionAmount": 1400,
      "transactionCode": 1701,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10001,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980160",
      "transactionAmount": 2300,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980170",
      "transactionAmount": 1450,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980180",
      "transactionAmount": 50,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980190",
      "transactionAmount": 1005,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET DEBIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980520199980200",
      "transactionAmount": 1024,
      "transactionCode": 7015,
      "transactionType": "D"
    },
    {
      "description": "Wall Mart LLC USA      Florida       US",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210521",
      "referenceNumber": "VT211410001000010000012",
      "transactionAmount": 2000,
      "transactionCode": 4006,
      "transactionType": "D"
    },
    {
      "description": "Australia Bank LLC     Sydney        AU",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210521",
      "referenceNumber": "VT211410001000010000016",
      "transactionAmount": 2600,
      "transactionCode": 4511,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980521199980010",
      "transactionAmount": 2000,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210520",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210520",
      "referenceNumber": "19999999980521199980020",
      "transactionAmount": 2600,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "Wall Mart LLC USA      Sydney        AU",
      "effectiveDate": "20210521",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210525",
      "referenceNumber": "VT211450002000010000003",
      "transactionAmount": 800,
      "transactionCode": 4000,
      "transactionType": "D"
    },
    {
      "description": "Westpac ATM              Sydney CBD   AU",
      "effectiveDate": "20210525",
      "paymentInstrumentId": "0009543491000008124",
      "planId": 10002,
      "postingDate": "20210525",
      "referenceNumber": "ST211450004000010000029",
      "transactionAmount": 500,
      "transactionCode": 6701,
      "transactionType": "D"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210521",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210521",
      "referenceNumber": "19999999980525199980010",
      "transactionAmount": 800,
      "transactionCode": 7016,
      "transactionType": "C"
    },
    {
      "description": "DEBIT CARD OFFSET CREDIT",
      "effectiveDate": "20210525",
      "paymentInstrumentId": "0002000010000066752",
      "planId": 10002,
      "postingDate": "20210525",
      "referenceNumber": "19999999980525199980020",
      "transactionAmount": 500,
      "transactionCode": 7016,
      "transactionType": "C"
    }
  ]
}
```
### Error Response Payload

```json

```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5TD4002SB` | No account on File |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*