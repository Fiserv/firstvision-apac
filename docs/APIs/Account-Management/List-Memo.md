# List Memos

This service will retrieve all ASM memos for the associated Account number requested. 

## Endpoint

`GET /v1/accounts/{accountId}/memoList`

## Payload Example

### Request Payload

>Should be empty. 
>
>***Account id should be sent as path variable.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/accounts/{accountId}/memoList).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. | 

### Successful Response Payload

```json
{
  "memoLines": [
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2706595700",
      "historyDate": "27/01/2022",
      "historyTime": 65958,
      "recordType": "M",
      "referralRepresentativeId": "NAB",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2707381500",
      "historyDate": "27/01/2022",
      "historyTime": 73815,
      "recordType": "M",
      "referralRepresentativeId": "NAB",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2707485600",
      "historyDate": "27/01/2022",
      "historyTime": 74857,
      "recordType": "M",
      "referralRepresentativeId": "NAB",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2707571300",
      "historyDate": "27/01/2022",
      "historyTime": 75713,
      "recordType": "M",
      "referralRepresentativeId": "NAB",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2710042600",
      "historyDate": "27/01/2022",
      "historyTime": 100427,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2710131900",
      "historyDate": "27/01/2022",
      "historyTime": 101319,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2710193300",
      "historyDate": "27/01/2022",
      "historyTime": 101933,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "2723304300",
      "historyDate": "27/01/2022",
      "historyTime": 233043,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "0",
      "historyDate": "31/01/2022",
      "historyTime": 15751,
      "recordType": "N",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "C"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "0",
      "historyDate": "31/01/2022",
      "historyTime": 22104,
      "recordType": "N",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "C"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "0",
      "historyDate": "31/01/2022",
      "historyTime": 22543,
      "recordType": "N",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "C"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "3808170000",
      "historyDate": "07/02/2022",
      "historyTime": 81700,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "3809461100",
      "historyDate": "07/02/2022",
      "historyTime": 94611,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4102330700",
      "historyDate": "10/02/2022",
      "historyTime": 23309,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107100400",
      "historyDate": "10/02/2022",
      "historyTime": 71004,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107185200",
      "historyDate": "10/02/2022",
      "historyTime": 71852,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107201700",
      "historyDate": "10/02/2022",
      "historyTime": 72017,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107224400",
      "historyDate": "10/02/2022",
      "historyTime": 72244,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107381400",
      "historyDate": "10/02/2022",
      "historyTime": 73815,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    },
    {
      "accountId": "0006000011000000160",
      "actionCode": "AINQ",
      "actionDescription": "ACCOUNT INQ",
      "actionNote1": "",
      "actionNote2": "",
      "actionNote3": "",
      "actionNote4": "",
      "actionNote5": "",
      "businessUnit": 600,
      "caseNumber": "4107405300",
      "historyDate": "10/02/2022",
      "historyTime": 74053,
      "recordType": "M",
      "referralRepresentativeId": "",
      "referredAsmOrganization": 0,
      "status": "O"
    }
  ]
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "240010",
    "instance": "/v1/accounts/0006000011000000161/memoList",
    "invalid-params": [
      "businessUnit: The maximum value for this field is 999"
    ],
    "source": "APT",
    "status": 400,
    "title": "Constraint(s) Violated"
  }
]
```

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
