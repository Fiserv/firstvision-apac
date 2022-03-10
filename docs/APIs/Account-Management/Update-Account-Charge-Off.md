# Update Account Charge-Off

 This service is used to update account status.

## Endpoint

`PUT /v1/accounts/{accountNumber}/chargeoff`

## Payload Example

### Request Payload

```json
{
  "dateofNotificationReceived": "01/01/2018",
  "systemDefinedChargeOffReason": "C"
} 
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountNumber}/chargeoff).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountNumber` | Path Variable | *String* | 19 | Account Number of the cardholder. | 
| `businessUnit` | Query Parameter |*number* | 3 | Identification number of the organization associated with the account. |
| `dateofNotificationReceived` | Payload |*Date* | DD/MM/YYYY | Date on which a bankruptcy notification was received or date on which a fraudulent loan was discovered. |
| `systemDefinedChargeOffReason` | Payload |*string* | 1 | Code that identifies the charge-off reason for the account |

### Successful Response Payload

```json
{
  "accountNumber": "0000000001000000057",
  "businessUnit": "600",
  "chargeOffStatus": "3",
  "dateofNotificationReceived": "01/01/2018",
  "numberofChargeOffDays": "0",
  "systemDefinedChargeOffReason": "C"
}
```

### Error Response Payload

```json
{
  "errorCode": "V5BS0109SA",
  "errorMessage": "Invalid Internal Status"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS0010SF` | Update Request - Record not found |
| `V5BS0109SA` | Invalid Internal Status |
| `V5BS0109SB` | PROC Date must be greater than greatest EXP date For purged Acct | 
| `V5BS0109SC` | Status cannot change to closed when insurance is Active | 
| `V5BS0110EB` | RSN code must be defined |
| `V5BS0110EC` | Cannot Use Chgoff RSN defined In Logo Lvl For Chgoff Sta'2' | 
| `V5BS0110SA` | Entered Auto C/O RSN code - CHG To manual Reason |   
| `V5BS0110SD` | Cannot use Reason defined for auto chgoff accts |          
| `V5BS0110SE` | This charge Off status is not allowed For Edit Or acct has dispute | 
| `V5BS0110SF` | Cannot charge Off an account with A zero Or credit balance |        
| `V5BS0110SG` | Cannot reset chargeoff On account when days Is > 0 |                
| `V5BS0110SH` | Chgoff status update Is not allowed during add |                   
| `V5BS0184SA` | Not A valid date |
| `V5BS0125SA` | Cannot set A block code On A billing account |
| `V5BS0125SB` | Block code 1 must be alphabetic |
| `V5BS0125SC` | Block code 1 cannot be Replaced With One Of A Lower priority |
| `V5BS0127SA` | Cannot Set A block Code On A Billing account |
| `V5BS0127SB` | Block code 2 must be alphabetic |
| `V5BS0127SC` | Block code cannot be Replaced With One Of A Lower priority |