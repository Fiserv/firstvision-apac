# Update Delinquency

This service is used to reage the account, reaging an account is normally done to cause an account to appear less delinquent by reducing the delinquency level. Also, user can adjust the account level due buckets or plan level dues if there is any discrepancy.

## Endpoint

`PUT /v1/accounts/{accountId}/delinquency`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Account id should be sent as path variable.***

<!--
type: tab
-->

```json
{
  "accountDueDetails": {
    "120daysDelinquentAmount": "0.00",
    "150daysDelinquentAmount": "0.00",
    "180daysDelinquentAmount": "0.00",
    "210daysDelinquentAmount": "0.00",
    "30daysDelinquentAmount": "0.00",
    "60daysDelinquentAmount": "0.00",
    "90daysDelinquentAmount": "0.00",
    "currentDueAmount": "0.00",
    "pastDueAmount": "0.00"
  },
  "cycleDue": "1",
  "planDueDetails": {
    "totalDue01Amount": "20.00",
    "totalDue02Amount": "0.00",
    "totalDue03Amount": "0.00",
    "totalDue04Amount": "0.00",
    "totalDue05Amount": "0.00",
    "totalDue06Amount": "0.00",
    "totalDue07Amount": "0.00",
    "totalDue08Amount": "0.00",
    "totalDue09Amount": "0.00",
    "totalDue10Amount": "0.00",
    "totalDue11Amount": "0.00",
    "totalDue12Amount": "0.00",
    "totalDue13Amount": "0.00",
    "totalDue14Amount": "0.00",
    "totalDue15Amount": "0.00",
    "totalDue16Amount": "0.00",
    "totalDue17Amount": "0.00",
    "totalDue18Amount": "0.00",
    "totalDue19Amount": "0.00",
    "totalDue20Amount": "0.00",
    "totalDue21Amount": "0.00",
    "totalDue22Amount": "0.00",
    "totalDue23Amount": "0.00",
    "totalDue24Amount": "0.00",
    "totalDue25Amount": "0.00",
    "totalDue26Amount": "0.00",
    "totalDue27Amount": "0.00",
    "totalDue28Amount": "0.00",
    "totalDue29Amount": "0.00",
    "totalDue30Amount": "0.00",
    "totalDue31Amount": "0.00",
    "totalDue32Amount": "0.00",
    "totalDue33Amount": "0.00",
    "totalDue34Amount": "0.00",
    "totalDue35Amount": "0.00",
    "totalDue36Amount": "0.00",
    "totalDue37Amount": "0.00",
    "totalDue38Amount": "0.00",
    "totalDue39Amount": "0.00",
    "totalDue40Amount": "0.00",
    "totalDue41Amount": "0.00",
    "totalDue42Amount": "0.00",
    "totalDue43Amount": "0.00",
    "totalDue44Amount": "0.00",
    "totalDue45Amount": "0.00",
    "totalDue46Amount": "0.00",
    "totalDue47Amount": "0.00",
    "totalDue48Amount": "0.00",
    "totalDue49Amount": "0.00",
    "totalDue50Amount": "0.00",
    "totalDue51Amount": "0.00",
    "totalDue52Amount": "0.00",
    "totalDue53Amount": "0.00",
    "totalDue54Amount": "0.00",
    "totalDue55Amount": "0.00",
    "totalDue56Amount": "0.00",
    "totalDue57Amount": "0.00",
    "totalDue58Amount": "0.00",
    "totalDue59Amount": "0.00",
    "totalDue60Amount": "0.00",
    "totalDue61Amount": "0.00",
    "totalDue62Amount": "0.00",
    "totalDue63Amount": "0.00",
    "totalDue64Amount": "0.00",
    "totalDue65Amount": "0.00",
    "totalDue66Amount": "0.00",
    "totalDue67Amount": "0.00",
    "totalDue68Amount": "0.00",
    "totalDue69Amount": "0.00",
    "totalDue70Amount": "0.00",
    "totalDue71Amount": "0.00",
    "totalDue72Amount": "0.00",
    "totalDue73Amount": "0.00",
    "totalDue74Amount": "0.00",
    "totalDue75Amount": "0.00",
    "totalDue76Amount": "0.00",
    "totalDue77Amount": "0.00",
    "totalDue78Amount": "0.00",
    "totalDue79Amount": "0.00",
    "totalDue80Amount": "0.00",
    "totalDue81Amount": "0.00",
    "totalDue82Amount": "0.00",
    "totalDue83Amount": "0.00",
    "totalDue84Amount": "0.00",
    "totalDue85Amount": "0.00",
    "totalDue86Amount": "0.00",
    "totalDue87Amount": "0.00",
    "totalDue88Amount": "0.00",
    "totalDue89Amount": "0.00",
    "totalDue90Amount": "0.00",
    "totalDue91Amount": "0.00",
    "totalDue92Amount": "0.00",
    "totalDue93Amount": "0.00",
    "totalDue94Amount": "0.00",
    "totalDue95Amount": "0.00",
    "totalDue96Amount": "0.00",
    "totalDue97Amount": "0.00",
    "totalDue98Amount": "0.00",
    "totalDue99Amount": "0.00"
  }
}
```

<!--
type: tab
-->

```json
{
  "accountDueDetails": {
    "120daysDelinquentAmount": "$0.00",
    "150daysDelinquentAmount": "$0.00",
    "180daysDelinquentAmount": "$0.00",
    "210daysDelinquentAmount": "$0.00",
    "30daysDelinquentAmount": "$0.00",
    "60daysDelinquentAmount": "$0.00",
    "90daysDelinquentAmount": "$0.00",
    "currentDueAmount": "$0.00",
    "pastDueAmount": "$0.00"
  },
  "accountId": "0002000010000066752",
  "businessUnit": 200,
  "cycleDue": "1",
  "planDueDetails": {
    "totalDue01Amount": "$20.00",
    "totalDue02Amount": "$0.00",
    "totalDue03Amount": "$0.00",
    "totalDue04Amount": "$0.00",
    "totalDue05Amount": "$0.00",
    "totalDue06Amount": "$0.00",
    "totalDue07Amount": "$0.00",
    "totalDue08Amount": "$0.00",
    "totalDue09Amount": "$0.00",
    "totalDue10Amount": "$0.00",
    "totalDue11Amount": "$0.00",
    "totalDue12Amount": "$0.00",
    "totalDue13Amount": "$0.00",
    "totalDue14Amount": "$0.00",
    "totalDue15Amount": "$0.00",
    "totalDue16Amount": "$0.00",
    "totalDue17Amount": "$0.00",
    "totalDue18Amount": "$0.00",
    "totalDue19Amount": "$0.00",
    "totalDue20Amount": "$0.00",
    "totalDue21Amount": "$0.00",
    "totalDue22Amount": "$0.00",
    "totalDue23Amount": "$0.00",
    "totalDue24Amount": "$0.00",
    "totalDue25Amount": "$0.00",
    "totalDue26Amount": "$0.00",
    "totalDue27Amount": "$0.00",
    "totalDue28Amount": "$0.00",
    "totalDue29Amount": "$0.00",
    "totalDue30Amount": "$0.00",
    "totalDue31Amount": "$0.00",
    "totalDue32Amount": "$0.00",
    "totalDue33Amount": "$0.00",
    "totalDue34Amount": "$0.00",
    "totalDue35Amount": "$0.00",
    "totalDue36Amount": "$0.00",
    "totalDue37Amount": "$0.00",
    "totalDue38Amount": "$0.00",
    "totalDue39Amount": "$0.00",
    "totalDue40Amount": "$0.00",
    "totalDue41Amount": "$0.00",
    "totalDue42Amount": "$0.00",
    "totalDue43Amount": "$0.00",
    "totalDue44Amount": "$0.00",
    "totalDue45Amount": "$0.00",
    "totalDue46Amount": "$0.00",
    "totalDue47Amount": "$0.00",
    "totalDue48Amount": "$0.00",
    "totalDue49Amount": "$0.00",
    "totalDue50Amount": "$0.00",
    "totalDue51Amount": "$0.00",
    "totalDue52Amount": "$0.00",
    "totalDue53Amount": "$0.00",
    "totalDue54Amount": "$0.00",
    "totalDue55Amount": "$0.00",
    "totalDue56Amount": "$0.00",
    "totalDue57Amount": "$0.00",
    "totalDue58Amount": "$0.00",
    "totalDue59Amount": "$0.00",
    "totalDue60Amount": "$0.00",
    "totalDue61Amount": "$0.00",
    "totalDue62Amount": "$0.00",
    "totalDue63Amount": "$0.00",
    "totalDue64Amount": "$0.00",
    "totalDue65Amount": "$0.00",
    "totalDue66Amount": "$0.00",
    "totalDue67Amount": "$0.00",
    "totalDue68Amount": "$0.00",
    "totalDue69Amount": "$0.00",
    "totalDue70Amount": "$0.00",
    "totalDue71Amount": "$0.00",
    "totalDue72Amount": "$0.00",
    "totalDue73Amount": "$0.00",
    "totalDue74Amount": "$0.00",
    "totalDue75Amount": "$0.00",
    "totalDue76Amount": "$0.00",
    "totalDue77Amount": "$0.00",
    "totalDue78Amount": "$0.00",
    "totalDue79Amount": "$0.00",
    "totalDue80Amount": "$0.00",
    "totalDue81Amount": "$0.00",
    "totalDue82Amount": "$0.00",
    "totalDue83Amount": "$0.00",
    "totalDue84Amount": "$0.00",
    "totalDue85Amount": "$0.00",
    "totalDue86Amount": "$0.00",
    "totalDue87Amount": "$0.00",
    "totalDue88Amount": "$0.00",
    "totalDue89Amount": "$0.00",
    "totalDue90Amount": "$0.00",
    "totalDue91Amount": "$0.00",
    "totalDue92Amount": "$0.00",
    "totalDue93Amount": "$0.00",
    "totalDue94Amount": "$0.00",
    "totalDue95Amount": "$0.00",
    "totalDue96Amount": "$0.00",
    "totalDue97Amount": "$0.00",
    "totalDue98Amount": "$0.00",
    "totalDue99Amount": "$0.00"
  }
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
    "instance": "/v1/accounts/0006000011000000590/delinquency",
    "invalid-params": [
      "V5D24201SA: Reage cycle due flag is not valid"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/accounts/{accountId}/delinquency).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `accountId` | Path Variable | *string* | 19 | Unique identification number for cardholder billing account. |

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5BS9981SF` | Record not Found |
| `V5D24201SA` | Reage cycle due flag is not valid |
| `V5D24209SA` | Error processing current balance |
| `V5D24207SA` | Reage CD flag not valid on this plan |
| `V5D24205SA` | Plan is deferred and total due not zeroes |
| `V5D24203SA` | Curr due field entered - Reage CD not allowed |
| `V5D24206SA` | Calculated balance is greater than curr bal |
| `V5D24210SA` | Total plan balance does not match with base segment bal |
| `V5D24208SA` | Computed bal is more than base sgmt bal & diff in total is 00000000000000000 |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
