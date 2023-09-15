# Update Token Status

This API is used to update the token status for a given payment instrument Id and wallet token number for Visa and Mastercard schemes.

## Endpoint

`PUT /v1/cards/{paymentInstrumentId}/tokenStatus`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "schemeTokenNumber": "5077400005048482515",
  "status": "1"
}
```

<!--
type: tab
-->

```json
{
  "businessUnit": 100,
  "paymentInstrumentId": "0009846801010273613",
  "status": "1"
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
    "instance": "/v1/cards/0009846801010273613/tokenStatus",
    "invalid-params": [
      "V5Z74052EB: TOKEN NBR MUST BE 13 TO 19 DIGITS"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```
<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/cards/{paymentInstrumentId}/tokenStatus).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `paymentInstrumentId` | Path Variable | *string* | 19 | Unique alternate identification number associated with Payment Card Number. |
| `schemeTokenNumber` | Payload | *string* | 19 | Token number assigned by the Tokenization Service. |
| `status` | Payload | *string* | 01 | This field indicate the status of token. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5Z74099SE` | Not signed on to visanet, outgoing requests not possible |
| `V5Z74052EB` | Invalid token details |
| `V5Z74052EA` | Selected token number is spaces or invalid |
| `V5Z74052EB` | Token nbr must be 13 to 19 digits |
| `V5Z74099SE` | Not signed on to visanet, outgoing requests not possible |
| `V5Z74051EA` | Token not received from OFSA |
| `V5Z74051EB` | Please select action code |
| `V5Z74051EC` | Token not found on token master file |
| `V5Z74001IB` | Request accepted successfully |
| `V5Z74013SB` | Account number is invalid |
| `V5Z74099SD` | Not signed on to visanet, outgoing requests not possible |
| `V5LC4002SA` | Input org is not matching with card numbers org |
| `V7A84001SA` | System record not loaded properly |
| `V7A84001EA` | End-of-day cutoff being processed.try again soon |
| `V7A84001EB` | After hours update in progress,cannot process at this time |
| `V7A84001EC` | System control record, processing status is invalid |
| `V7A84040SA` | No link to banknet, outgoing requests not possible |
| `V7A84040SB` | Not signed on to banknet, outgoing requests not possible |
| `V7A84050SA` | Please give the input details |
| `V7A84053SA` | Select only one option, token or pan update |
| `V7A84053SB` | Select at least one option, token or pan update |
| `V7A84053SC` | Token update selected, no token update data provide |
| `V7A84054SA` | PAN, PAN expire date, PAN sequence number required |
| `V7A84054SB` | PAN must be 16 to 19 digits |
| `V7A84054SC` | Token must be numeric |
| `V7A84054SD` | PAN not found in the master card file |
| `V7A84054SE` | PAN logo not same |
| `V7A84055SA` | New PAN expire date required |
| `V7A84055SB` | PAN expire date invalid |
| `V7A84055SC` | PAN expire date invalid |
| `V7A84056SA` | Invalid seq number |
| `V7A84057SA` | Token must be 16 to 19 digits |
| `V7A84057SB` | Token must be numeric |
| `V7A84060SA` | Token must be 13 to 19 digits |
| `V7A84060SB` | Token must be numeric |
| `V7A84052EA` | Invalid value: value must be 0 |
| `V7A84003SA` | Item error, for responce queue |
| `V7A84004SA` | Maping file indicator must be A or M |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
