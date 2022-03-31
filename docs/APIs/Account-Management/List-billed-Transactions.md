# List billed Transactions

The service provides list of transactions along with detail information of transactions posted in the last statement cycle.

## Endpoint

`GET /v1/accounts/{accountNumber}/transactions/lastStatement`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as and path variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/transactions/lastStatement).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique identification number of the Account. | 

### Successful Response Payload

```json

{
  "accountRelationship": "0002000010000066752",
  "statementDate": "30/06/2021",
  "transactionListRes": [
    {
      "authorizationCode": "021447",
      "creditPlan": 10002,
      "effectiveDate": "13/05/2021",
      "logicModule": 1,
      "postingDate": "13/05/2021",
      "transactionAmount": "$10.00",
      "transactionCode": 4000,
      "transactionDescription": "Australia Bank         Melbaourne    AU",
      "transactionReferenceNumber": "VT211330002000010000025",
      "transactionType": "D"
    },
    {
      "authorizationCode": "021447",
      "creditPlan": 10002,
      "effectiveDate": "13/05/2021",
      "logicModule": 7,
      "postingDate": "13/05/2021",
      "transactionAmount": "$1.00",
      "transactionCode": 4579,
      "transactionDescription": "Australia Bank         Melbaourne    AU",
      "transactionReferenceNumber": "VT211330002000010000026",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "13/05/2021",
      "logicModule": 4,
      "postingDate": "13/05/2021",
      "transactionAmount": "$10.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980513199980010",
      "transactionType": "C"
    },
    {
      "authorizationCode": "022709",
      "creditPlan": 10002,
      "effectiveDate": "18/05/2021",
      "logicModule": 2,
      "postingDate": "18/05/2021",
      "transactionAmount": "$15.01",
      "transactionCode": 4567,
      "transactionDescription": "Wall Mart LLC AUS      Sydney        AU",
      "transactionReferenceNumber": "VT211380004000010000001",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "18/05/2021",
      "logicModule": 3,
      "postingDate": "18/05/2021",
      "transactionAmount": "$15.01",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980518199980010",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023754",
      "creditPlan": 10002,
      "effectiveDate": "19/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$11.11",
      "transactionCode": 4000,
      "transactionDescription": "Wall Mart LLC          Sydney        AU",
      "transactionReferenceNumber": "VT211400002000010000010",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023911",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$25.00",
      "transactionCode": 6800,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000064",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023912",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$21.00",
      "transactionCode": 6804,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000065",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023912",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$4.00",
      "transactionCode": 6806,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000066",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023913",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.00",
      "transactionCode": 6804,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000067",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023913",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$5.00",
      "transactionCode": 6806,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000068",
      "transactionType": "D"
    },
    {
      "authorizationCode": "283763",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.03",
      "transactionCode": 4004,
      "transactionDescription": "Wall Mart LLC AUS      Sydney        AU",
      "transactionReferenceNumber": "VT211400002000010000042",
      "transactionType": "D"
    },
    {
      "authorizationCode": "283781",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.21",
      "transactionCode": 4545,
      "transactionDescription": "Australia Bank LLC     Sydney        AU",
      "transactionReferenceNumber": "VT211400002000010000048",
      "transactionType": "D"
    },
    {
      "authorizationCode": "283785",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.25",
      "transactionCode": 4561,
      "transactionDescription": "Australia Bank LLC     Sydney        AU",
      "transactionReferenceNumber": "VT211400002000010000050",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023902",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 30,
      "postingDate": "20/05/2021",
      "transactionAmount": "$21.00",
      "transactionCode": 6816,
      "transactionDescription": "EDAF EFTPOS              PEASANT NEST AU",
      "transactionReferenceNumber": "ST211400003000010000059",
      "transactionType": "C"
    },
    {
      "authorizationCode": "023904",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 30,
      "postingDate": "20/05/2021",
      "transactionAmount": "$22.00",
      "transactionCode": 6816,
      "transactionDescription": "EDAF EFTPOS              PEASANT NEST AU",
      "transactionReferenceNumber": "ST211400003000010000060",
      "transactionType": "C"
    },
    {
      "authorizationCode": "023905",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 30,
      "postingDate": "20/05/2021",
      "transactionAmount": "$23.00",
      "transactionCode": 6818,
      "transactionDescription": "EDAF EFTPOS              PEASANT NEST AU",
      "transactionReferenceNumber": "ST211400003000010000062",
      "transactionType": "C"
    },
    {
      "authorizationCode": "023913",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 2,
      "postingDate": "20/05/2021",
      "transactionAmount": "$14.50",
      "transactionCode": 6805,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000069",
      "transactionType": "C"
    },
    {
      "authorizationCode": "023913",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 2,
      "postingDate": "20/05/2021",
      "transactionAmount": "$0.50",
      "transactionCode": 6807,
      "transactionDescription": "CHIP EFTPOS              PHEASANTS NESAU",
      "transactionReferenceNumber": "ST211400003000010000070",
      "transactionType": "C"
    },
    {
      "authorizationCode": "283765",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 2,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.05",
      "transactionCode": 4106,
      "transactionDescription": "Wall Mart LLC USA      Florida       US",
      "transactionReferenceNumber": "VT211400002000010000029",
      "transactionType": "C"
    },
    {
      "authorizationCode": "283765",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 99,
      "postingDate": "20/05/2021",
      "transactionAmount": "$0.00",
      "transactionCode": 96,
      "transactionDescription": "05/20/21          5.03  USD",
      "transactionReferenceNumber": "VT211400002000010000029",
      "transactionType": "M"
    },
    {
      "authorizationCode": "283784",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 2,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.24",
      "transactionCode": 4560,
      "transactionDescription": "Australia Bank LLC     Sydney        AU",
      "transactionReferenceNumber": "VT211400002000010000041",
      "transactionType": "C"
    },
    {
      "authorizationCode": "023905",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 31,
      "postingDate": "20/05/2021",
      "transactionAmount": "$23.00",
      "transactionCode": 6819,
      "transactionDescription": "EDAF EFTPOS              PEASANT NEST AU",
      "transactionReferenceNumber": "ST211400003000010000063",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "19/05/2021",
      "logicModule": 4,
      "postingDate": "19/05/2021",
      "transactionAmount": "$11.11",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980010",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$25.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980020",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$21.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980030",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$4.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980040",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980050",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$5.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980060",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.03",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980070",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.21",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980080",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.25",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980520199980090",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10001,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$21.00",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980100",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$13.00",
      "transactionCode": 2701,
      "transactionDescription": "PRINCIPAL DEBIT ADJUSTMENT",
      "transactionReferenceNumber": "19999999980520199980110",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10001,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$13.00",
      "transactionCode": 1701,
      "transactionDescription": "PRINCIPAL CREDIT ADJUSTMENT",
      "transactionReferenceNumber": "19999999980520199980120",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10001,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$22.00",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980130",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$14.00",
      "transactionCode": 2701,
      "transactionDescription": "PRINCIPAL DEBIT ADJUSTMENT",
      "transactionReferenceNumber": "19999999980520199980140",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10001,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$14.00",
      "transactionCode": 1701,
      "transactionDescription": "PRINCIPAL CREDIT ADJUSTMENT",
      "transactionReferenceNumber": "19999999980520199980150",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10001,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$23.00",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980160",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$14.50",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980170",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$0.50",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980180",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.05",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980190",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 3,
      "postingDate": "20/05/2021",
      "transactionAmount": "$10.24",
      "transactionCode": 7015,
      "transactionDescription": "DEBIT CARD OFFSET DEBIT",
      "transactionReferenceNumber": "19999999980520199980200",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023862",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "21/05/2021",
      "transactionAmount": "$20.00",
      "transactionCode": 4006,
      "transactionDescription": "Wall Mart LLC USA      Florida       US",
      "transactionReferenceNumber": "VT211410001000010000012",
      "transactionType": "D"
    },
    {
      "authorizationCode": "023862",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 99,
      "postingDate": "21/05/2021",
      "transactionAmount": "$0.00",
      "transactionCode": 96,
      "transactionDescription": "05/20/21         10.00  USD",
      "transactionReferenceNumber": "VT211410001000010000012",
      "transactionType": "M"
    },
    {
      "authorizationCode": "023916",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 1,
      "postingDate": "21/05/2021",
      "transactionAmount": "$26.00",
      "transactionCode": 4511,
      "transactionDescription": "Australia Bank LLC     Sydney        AU",
      "transactionReferenceNumber": "VT211410001000010000016",
      "transactionType": "D"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$20.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980521199980010",
      "transactionType": "C"
    },
    {
      "authorizationCode": " ",
      "creditPlan": 10002,
      "effectiveDate": "20/05/2021",
      "logicModule": 4,
      "postingDate": "20/05/2021",
      "transactionAmount": "$26.00",
      "transactionCode": 7016,
      "transactionDescription": "DEBIT CARD OFFSET CREDIT",
      "transactionReferenceNumber": "19999999980521199980020",
      "transactionType": "C"
    },
    {
      "authorizationCode": "025052",
      "creditPlan": 10002,
      "effectiveDate": "21/05/2021",
      "logicModule": 1,
      "postingDate": "25/05/2021",
      "transactionAmount": "$8.00",
      "transactionCode": 4000,
      "transactionDescription": "Wall Mart LLC USA      Sydney        AU",
      "transactionReferenceNumber": "VT211450002000010000003",
      "transactionType": "D"
    },
    {
      "authorizationCode": "027182",
      "creditPlan": 10002,
      "effectiveDate": "25/05/2021",
      "logicModule": 1,
      "postingDate": "25/05/2021",
      "transactionAmount": "$5.00",
      "transactionCode": 6701,
      "transactionDescription": "Westpac ATM              Sydney CBD   AU",
      "transactionReferenceNumber": "ST211450004000010000029",
      "transactionType": "D"
    }
  ],
  "transactionNextToken": "2000002000010000066752202118q50052"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5S34003SA",
  "errorMessage": "No statement history information found on file"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0011SF` | Update Request - Record add pending |
| `V5BS4001EA` | Invalid business unit |
| `V5BS4001SC` | Business unit is in purged status |
| `V5BS4002SA` | Invalid account number |  
| `V5S34003SA` | No statement history information found on file |
