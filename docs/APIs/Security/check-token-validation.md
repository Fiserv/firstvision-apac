# Check Token Validation

This API is used to validate if the given oauth token is valid/invalid.

## Endpoint

`POST /v1/api/oauth/validateToken`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->


>Should be empty. 
>
>***Token should be sent as query parameter.***

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