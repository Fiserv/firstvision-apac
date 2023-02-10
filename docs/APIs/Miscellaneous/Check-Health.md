# Check Health

This API is used to verify health of credit management system and authorization system. This service gives the detail whether the system is active to respond on authorization requests, service requests etc.

## Endpoint

`GET /v1/misc/health`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***No input required.***

<!--
type: tab
-->

```json
{
  "creditManagementHealthStatus": "0",
  "authorizationHealthStatus": "0"
}
```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "240101",
    "instance": "/v1/misc/health",
    "invalid-params": [
      "Bearer token is invalid"
    ],
    "source": "AGT",
    "status": 401,
    "title": "Unauthorized"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/misc/health).

>***No mandatory fields required in input.***

### Error Codes

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*

