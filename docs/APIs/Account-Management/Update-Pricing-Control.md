# Update Pricing Control

This service is used update pricing control structure over an accounts. This service will update PCT Override, PCT Start Date, State Of Residency, State Of Issuance and PCT Expiry Date.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/accounts/{accountNumber}/pricingControls`

## Payload Example

### Request Payload

```json
{
  "pctOverride": "HCS",
  "stateOfResidency": "SX1",
  "stateOfIssuance": "SX1",
  "pctExpiryDate": "31/12/2025",
  "pctStartDate": "29/01/2022"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/pricingControls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `accountNumber` | Path Variable | *string* | 19 | Account Number of the cardholder. |
| `pCTOverride` | Payload | *string* | 3 | Code that identifies an existing Processing Control Table (PCT ID). | 
| `pCTStartDate` | Payload | *Date* | DD/MM/YYYY | Date on which the special pricing controls start for the account. | 
| `stateOfResidency` | Payload | *string* | 3 | Code that identifies the state, province, or country in which the account holder resides. | 
| `stateOfIssuance` | Payload | *string* | 3 | Code that identifies the state, province or country in which the account was issued. | 
| `pCTExpiryDate` | Payload | *Date* | DD/MM/YYYY | Date on which the special pricing controls expire for the account. |  

### Successful Response Payload

```json
{
  "businessUnit": 600,
  "pctOverride": "HCS",
  "stateOfResidency": "SX1",
  "stateOfIssuance": "SX1",
  "pctExpiryDate": "31/12/2025",
  "accountNumber": 6000011000000137,
  "pctStartDate": "29/01/2022"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0302SB",
  "errorMessage": "Issuance id not on usury table"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0302SB` | Issuance id not on usury table | 
| `V5BS0302SC` | Zero $$$$ in usury table for SOI | 
| `V5BS0302SD` | No pct rec found at this level | 
| `V5BS0302SE` | No active rates in processing control table | 
| `V5BS0302SF` | No file processing control table | 
| `V5BS0301SA` | Residence id not on usury table | 
| `V5BS0301SB` | Zero $$$ in usury table for SOR | 
| `V5BS0301SC` | Residence id can not be spaces | 
| `V5BS0301SD` | No pct rec found at this level | 
| `V5BS0301SE` | No active rates in processing control table | 
| `V5BS0301SF` | No file processing control table | 
| `V5BS0303SA` | No pct rec found at this level | 
| `V5BS0303SB` | No pct rec found at this level | 
| `V5BS0303SC` | No active rates in processing control table | 
| `V5BS0303SD` | No file processing control table | 
| `V5BS0304SA` | Pricing ctrl start/expiration dates conflict | 
| `V5BS0304SB` | Enter pricing ctrl when using dates | 
| `V5BS0304SC` | Start date less than the org next processing date | 
| `V5BS0304SD` | Expire date less than the org next processing date | 
