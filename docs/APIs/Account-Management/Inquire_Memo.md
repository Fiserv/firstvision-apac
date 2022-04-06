# Inquire Memo

 This service will retrieve all ASM memos for the associated Card/Account number requested. 

## Endpoint

`GET /v1/accounts/{accountNumber}/memoList`

## Payload Example

### Request Payload

>Should be empty. 
>
>***The Account Number should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountNumber}/memoList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *string* | 19 | Unique Identification number of the Account. | 

### Successful Response Payload

```json
{
  "memoListRes": [
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 65958,
      "historyTime": 65958,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "NAB",
      "caseNumber": "2706595700",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 73815,
      "historyTime": 73815,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "NAB",
      "caseNumber": "2707381500",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 74857,
      "historyTime": 74857,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "NAB",
      "caseNumber": "2707485600",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 75713,
      "historyTime": 75713,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "NAB",
      "caseNumber": "2707571300",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 100427,
      "historyTime": 100427,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "2710042600",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 101319,
      "historyTime": 101319,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "2710131900",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 101933,
      "historyTime": 101933,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "2710193300",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "27/01/2022",
      "alternateHistoryTime": 233043,
      "historyTime": 233043,
      "alternateHistoryDate": "27/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "2723304300",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "C",
      "historyDate": "31/01/2022",
      "alternateHistoryTime": 15751,
      "historyTime": 15751,
      "alternateHistoryDate": "31/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "0",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "N",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "C",
      "historyDate": "31/01/2022",
      "alternateHistoryTime": 22104,
      "historyTime": 22104,
      "alternateHistoryDate": "31/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "0",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "N",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "C",
      "historyDate": "31/01/2022",
      "alternateHistoryTime": 22543,
      "historyTime": 22543,
      "alternateHistoryDate": "31/01/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "0",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "N",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "07/02/2022",
      "alternateHistoryTime": 81700,
      "historyTime": 81700,
      "alternateHistoryDate": "07/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "3808170000",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "07/02/2022",
      "alternateHistoryTime": 94611,
      "historyTime": 94611,
      "alternateHistoryDate": "07/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "3809461100",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 23309,
      "historyTime": 23309,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4102330700",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 71004,
      "historyTime": 71004,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107100400",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 71852,
      "historyTime": 71852,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107185200",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 72017,
      "historyTime": 72017,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107201700",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 72244,
      "historyTime": 72244,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107224400",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 73815,
      "historyTime": 73815,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107381400",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    },
    {
      "accountNumber": "0006000011000000160",
      "status": "O",
      "historyDate": "10/02/2022",
      "alternateHistoryTime": 74053,
      "historyTime": 74053,
      "alternateHistoryDate": "10/02/2022",
      "referredAsmOrganization": 0,
      "referralRepresentativeId": "",
      "caseNumber": "4107405300",
      "actionDescription": "ACCOUNT INQ",
      "actionCode": "AINQ",
      "recordType": "M",
      "alternateOrganization": 600,
      "actionNote4": "",
      "actionNote3": "",
      "actionNote2": "",
      "actionNote1": "",
      "actionNote5": ""
    }
  ]
}

```

### Error Response Payload

```json
{
  "errorCode": "V5PH0004SF",
  "errorMessage": "Get Request - Record Not Found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5PH0004SF` | Get Request - Record Not Found |