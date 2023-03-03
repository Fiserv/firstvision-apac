# Transfer Lost Stolen Card

This API is used to block the lost or stolen card and request for the replacement card. Based on the input field values the corresponding actions will be taken like creating new card number and updating the existing card with block codes etc.

## Endpoint

`POST /v1/cards/lostStolenCardTransfer`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 600,
  "paymentInstrumentId": "0009544401000009195",
  "accountId": "0006000011000000178",
  "productId": 1,
  "cardReplacementIndicator": "0",
  "blockCode": "L",
  "startDate": "00/00/0000",
  "transferToAccountId": " ",
  "transferToCustomerId": " ",
  "effectiveDate": "00/00/0000",
  "processType": "0",
  "pinTransferIndicator": "N",
  "cardTransferActionCode": "CRTR",
  "cardTransferMemo": "Card transfer memo",
  "pinTransferActionCode": "PNTR",
  "pinTransferMemo": "PIN transfer memo"
}

```

<!--
type: tab
-->

```json
{
  "maskedPaymentInstrumentId": "0009544401XXXXX9208",
  "newPaymentInstrumentId": "0009544401000009208",
  "transferToAccountId": " ",
  "transferToCustomerId": " ",
  "effectiveDate": "19/08/2021"
}

```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/cards/lostStolenCardTransfer",
    "invalid-params": [
      "V5E14015EA: EMBOSSER RECORD NOT FOUND"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/lostStolenCardTransfer).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account. |
| `cardReplacementIndicator` | Payload | *number* | 1 |  Pass "1" for replacement of card or "0" to avoid initiation of card Replacement . |
| `blockCode` | Payload | *string* | 1 | Pass value as "L" to block the old card. |
| `ProductId` | Payload | *number* | 3 | Unique identification number of the product associated with the organization. Valid values are 1-998. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5E10004EA` | Invalid card number |
|`V5E14015EA` | Embosser record not found |
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
|`V5E14018EB` | Invalid card transfer action code |
|`V5E14020EB` | Invalid PIN transfer action code |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
