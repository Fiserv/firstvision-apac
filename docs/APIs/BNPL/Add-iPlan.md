# Add iPlan

This API is used to create iPlan record for given details in account Id, instalment amount and other details.

## Endpoint

`POST /v1/bnpl/addIplan`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "businessUnit": 700,
  "accountId": "0007000022102711404",
  "transactionAmount": "1000.00",
  "authorizationCode": "998271",
  "configurationTemplate": "TMPL10"
}
```

<!--
type: tab
-->

```json
{
    "sequenceNumber": "2",
    "accountId": "0007000022102711404",
    "businessUnit": 700
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "442201",
        "detail": "Please refer to invalid-params for error details",
        "title": "Unprocessable Entity",
        "instance": "/v1/bnpl/addIplan",
        "source": "VPL",
        "status": 422,
        "invalid-params": [
            "V5I14003EC: INVALID RETURN CODE - OFFER CODE FILE READ"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/bnpl/addIplan).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |
| `authorizationCode` | Payload | *string* | 6 | Field indicates the authorization code for transaction variant posting. |
| `transactionAmount` | Payload | *string* | 17 | Transaction amount to be converted into instalment. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5I14001EA` | Org in add pending status or not found |
| `V5I14001EB` | Org level BNPL functionality is not active |
| `V5I14001EC` | Logo in add pending status or not found |
| `V5I14001ED` | Logo level BNPL functionality is not active |
| `V5I14001SA` | Invalid organization entry |
| `V5I14002EA` | Account number invalid/not found/invalid status |
| `V5I14002EB` | Error accessing base segment file |
| `V5I14002EC` | BNPL pmt miss count has reached logo limit |
| `V5I14002SA` | Invalid account entry |
| `V5I14001SB` | No organization record on file or add pending |
| `V5I14001SC` | No system record |
| `V5I14002SC` | No account on file or add pending |
| `V5I14002SD` | No insurance products for the account  |
| `V5I14001SL` | No logo record |
| `V5I14002SG` | Default insurance table not found-end of process |
| `V5I14002SH` | Enrollment ins record not found-using default |
| `V5I14002SI` | Default insurance table not found-end of process |
| `V5I14002SJ` | State of resid record not found-using default |
| `V5I14002SK` | No insurance products for the account |
| `V5I14003EA` | Input or resolved BNPL offer has expired already |
| `V5I14003EB` | BNPL offer code bundle type cannot be added |
| `V5I14003EC` | Invalid return code - offer code file read |
| `V5I14003ED` | Real time OTB update failed - incorr acct int stat |
| `V5I14003EF` | Real time OTB update failed - AMMC file error |
| `V5I14003EG` | Real time OTB update failed - err access system rec |
| `V5I14003EH` | Real time OTB update failed - err access base seg |
| `V5I14003EI` | Real time OTB update failed - AMOA file error |
| `V5I14003EJ` | Real time OTB update failed - log file 3/4 problem |
| `V5I14003EK` | Real time OTB update failed - comm area length err |
| `V5I14003EL` | Real time OTB update failed - WMSW file access error fil |
| `V5I14003EM` | Real time OTB update failed - relationship record does not exist |
| `V5I14003EN` | Real time OTB update failed - relationship file unavailable |
| `V5I14003EO` | Real time OTB update failed - embosser card file unavailable |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
