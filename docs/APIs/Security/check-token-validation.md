# Check Token Validation

This API is used to validate if the given oauth token is valid/invalid.

## Endpoint

`POST /v1/api/oauth/validateToken`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImFsbCIsImNsaWVudF9pZCI6InZpc2lvbi1hcGktdXNlciIsImZpcnN0VmlzaW9uSWQiOiIwMDAwMEFVTkFCIiwiZXhwIjoxNzUwMzkyMDAwfQ.O6ZW0FnlWN09GqPeTEgWTQ9Gq6LPyt7BWTx65z7a0DKJQWBZ-pz29NX9xcuk-1ZdoLbKd_jPpwLNYGfS4KsuOLz1tQj1-teV2JO10DHxxthlG1-IGUIMyI5MivzNFlvLEG6TipqdQd3WdNl2juqlHKpDY86N0Z_Fg3n9igw4pFDzdGpHle5_4vGnl9PkYBA_WoWtgic05_63s5j6kmWbPkrV22NsHtOjJIh0sN1Q7sArecVnJCI7mwGVC5xasLGTO-Nn3hx6r8Y2mBv1Fv39LO_rUYcaK1RXS_xkoJV_3NdopGgfq4hp9F0naCKWxUxW1oaCaGCqk3p6xhkyDsJgaQ",
  "client_id": "vision-api-user",
  "client_secret": "abcdefghizklmnopponommnshfghzxxs"
}
```

<!--
type: tab
-->

```json
{
  "valid": true
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "140106",
    "instance": "/v1/api/oauth/validateToken",
    "invalid-params": [
      "Invalid client credentials"
    ],
    "source": "AGT",
    "status": 401,
    "title": "Unauthorized"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/api/oauth/validateToken).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `token` | Payload | *string* | 600 | JWT authorization token specific to the environment. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`140106` | Invalid client credentials |  


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
