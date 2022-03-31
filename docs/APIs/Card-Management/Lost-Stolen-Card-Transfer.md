# Transfer Lost Stolen Card 

This Lost or Stolen service is used to block the lost card and request for the replacement card. If the transfer is a product 
transfer, smart card transfer, or product graduation transfer, both the new account and the old account are available.

## Endpoint

`PUT /v1/cards/{cardNumber}/transfer`

## Payload Example
	
### Request Payload

```json
{
  "cardNumber": "0009846801010000461",
  "accountNumber": "0001000011000032014",
  "product": 1,
  "startDate": "0",
  "transferToAccount": "",
  "transferToCustomer": "",
  "effectiveDate": "0",
  "cardReplacementIndicator": "0",
  "blockCode": "L",
  "businessUnit": 600,
  "processType": "0"
}

```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{cardNumber}/transfer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Identification number of the organization associated with the account. |
| `cardNumber` | Path Variable | *string* | 19 | Token Number associated with the clear PAN. |
| `cardSequence` | Payload | *number* | 04 | A sequence number of the card in case of card scheme 2 else pass the default value of 0001. |
| `accountNumber` | Payload | *string* | 19 | Unique Identification number of the Account. |
| `action` | Payload | *string* | 19 | Pass value as "T" for transfer. |
| `cardReplacementIndicator` | Payload | *number* | 1 |  Pass "1" for replacement of card or "0" to avoid initiation of card Replacement . |
| `blockCode` | Payload | *string* | 1 | Pass value as "L" to block the old card. |

### Successful Response Payload

```json
{
  "cardNumber": "0004049400000006087",
  "effectiveDate": "19/08/2021",
  "maskCardNumber": "000404940XXXXXX6087",
  "transferToAccount": "",
  "transferToCustomer": ""
}

```

### Error Response Payload

```json
{
  "errorCode": "V5E10004EA",
  "errorMessage": "Invalid card number"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5E10004EA` | Invalid card number |
|`V5E10006EA` | Requested Business Unit is not found |
|`V5E11020EA` | Only reversal or transfer can be done |
|`V5E11021SA` | No reversal account number entered |
|`V5E11022SA` | Invalid transfer-to-account number |
|`V5E11022SB` | Transfer-to-account number invalid |
|`V5E11023EA` | Transfer-to-customer cannot be zero |
|`V5E11024EA` | Invalid block code |
|`V5E11024SA` | No lost/stolen/fraud block code in embosser |
|`V5E11025SA` | Please check block codes |
|`V5E11026EA` | Effective date not numeric |
|`V5E11027EA` | Invalid effective date |
|`V5E11028EA` | Effective date greater than next processing date |
|`V5E11029EA` | Transfer-to-account and Transfer-from-account cannot be same |
|`V5E11030SA` | Transfer-to-account not in base segment file |
|`V5E11033SA` | Record not active in customer file |
|`V5E11038EA` | Generated acct nbr is greater than base ending nbr |
|`V5E11039SA` | Reversal account not on file |
|`V5E11040SA` | Invalid check digit |
|`V5E11041SA` | Reversal cannot be processed during end-of-day |
|`V5E11043SA` | Transfer replacement indicator not zero |
|`V5E11045SA` | Transfer-from and Transfer-to accounts must be in the same logo |
|`V5E11046SA` | Transfer-to-acct has a balance and is not a fraud status acct |
|`V5E11065EA` | Record not found in Customer File |
|`V5E11066EA` | Invalid customer rec status |
|`V5E11069EA` | Record not found in Embosser File |
|`V5E11072EA` | Maximum nbr of 20 attempts made on customer nbr |
|`V5E11072EB` | Generated customer number is greater than ending customer number |
|`V5E11080EA` | Account and Card are not related to each other |
|`V5E14030EA` | Logo does not allow account number generation |
|`V5E14032EA` | Business unit does not allow customer number generation |
|`V5E10001SA` | System in after hours processing, re-try in few minutes |
|`V5E10002SA` | System in no-processing status,re-try in few minutes |