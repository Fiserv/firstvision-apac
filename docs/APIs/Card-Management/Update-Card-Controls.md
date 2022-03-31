# Update Card Controls

This service updates the card controls for a given card number like ECOM Active switch, ATM Flag, International ATM POS Flag, MOTO Flag and max Amount ATM/OTC/Retail etc.

Fields that are not provided in the request object will be initialised to their default values. All numeric fields are initialised to zero and alphanumeric fields initialised to spaces.

## Endpoint

`PUT /v1/cards/{cardNumber}/controls`

## Payload Example

### Request Payload

```json
{
"maximumAmountOtcCashAuthorizationsAllowed": 1000,
"maximumNumberRetailAuthorizationsAllowed": 2,
"motoFlag": "Y",
"payWaveSwitch": "N",
"maximumNumberOtcAuthorizationsAllowed": 5,
"cashBackTranFlag": "Y",
"maximumNumberAtmCashAuthorizationsAllowed": 10,
"singleOtcCashAuthorizationAllowed": 1200,
"maximumAmountSingleAtmTransactionAllowed": 1000,
"singleRetailAuthorizationAllowed": 1600,
"maximumAmountRetailAuthorizationsAllowed": 1000,
"ecomActiveSwitch": 0,
"atmFlag": "Y",
"posFlag": "N",
"maximumAmountAtmCashAuthorizationsAllowed": 1000,
"maximumAuthorizationsFrequnecy": 1,
"intAtmPosFlag": "Y"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/controls).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. | 
| `ecomActSW` | Payload | *string* | 1 |  ECOM Active switch. | 
| `aTMFlag` | Payload | *string* | 1 | ATM Flag. | 
| `iNTATMPOSFlag` | Payload | *string* | 1 | International ATM POS Flag. | 
| `mOTOFlag` | Payload | *string* | 1 | MOTO Flag. | 
| `pOSFlag` | Payload | *string* | 1 | POS Flag. | 
| `cashBackTranFlag` | Payload | *string* | 1 | Cash Back Transaction Flag. | 
| `pAYwaveFlag` | Payload | *string* | 1 | Pay Wave Switch. | 
| `maximumAuthorizationsFrequency` | Payload | *number* | 1 | Limit frequency to update. Valid values are a) "1"  Daily limits b) "2" Cycle to Date limits c) "3" Year to Date limits  |
| `maximumAmountSingle***TransactionAllowed` | Payload | *number* | 09 | Maximum amount of the Single ***(ATM / OTC / Retail) transaction allowed. |
| `maximumNumber***AuthorizationsAllowed` | Payload | *number* | 09 | Maximum number of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |
| `maximumAmount***AuthorizationsAllowed` | Payload | *number* | 17 | Maximum amount of the cumulatative ***(ATM / OTC / Retail) transaction allowed for a given frequency (daily / CTD/ YTD). |


### Successful Response Payload

```json
{
  "maximumAmountOtcCashAuthorizationsAllowed": 1000,
  "businessUnit": 100,
  "maximumNumberRetailAuthorizationsAllowed": 2,
  "motoFlag": "Y",
  "payWaveSwitch": "N",
  "maximumNumberOtcAuthorizationsAllowed": 5,
  "cashBackTranFlag": "Y",
  "maximumNumberAtmCashAuthorizationsAllowed": 10,
  "singleOtcCashAuthorizationAllowed": 1200,
  "maximumAmountSingleAtmTransactionAllowed": 1000,
  "singleRetailAuthorizationAllowed": 1600,
  "maximumAmountRetailAuthorizationsAllowed": 1000,
  "ecomActiveSwitch": 0,
  "atmFlag": "Y",
  "posFlag": "N",
  "maximumAmountAtmCashAuthorizationsAllowed": 1000,
  "maximumAuthorizationsFrequnecy": 1,
  "intAtmPosFlag": "Y",
  "cardNumber": 9846801010434752
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED8120CX",
  "errorMessage": "Saving acct nbr(or) cheque acct any one should be value"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED8120CX` | Saving acct nbr(or)Cheque acct any one should be value |        
| `V5ED0328EA` | Maximum freq input not allowed when no auth limit overrd | 
| `V5ED0319ED` | ATM cash AMT field update is not allowed | 
| `V5ED0319EF` | New ATM Cash Amt Is greater than allowable Limit | 
| `V5ED0320EE` | ATM Cash Nbr field update is not allowed | 
| `V5ED0321EH` | Txn Limit ATM field update is not allowed | 
| `V5ED0322EF` | OTC cash Amt field update is not allowed | 
| `V5ED0323EG` | OTC cash nbr field update is not allowed | 
| `V5ED0324EI` | TXN Limit Otc field update is not allowed | 
| `V5ED0325EB` | Retail amt field update is not allowed | 
| `V5ED0325EC` | New retail amt is greater than allowable limit | 
| `V5ED0326EC` | Retail nbr field update is not allowed | 
| `V5ED0327EJ` | Txn limit retail field update is not allowed | 