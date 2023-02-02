# Validate Access Token

This service is used to validate the given Access Token. Based on token validity a "valid=true" / "valid=false" is returned to user

## Endpoint

`GET /v1/api/oauth/validateToken`

## Payload Example

### Request Payload

>Should be empty. 
>
>***token value is sent as Query Parameter.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/getAccessToken).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `token` | Query Parameter | *string* | 1000 | Token which needs to be validated. |

### Successful Response Payload

```json
{
"valid": "true"
}
```

### Error Response Payload

```json
{
"valid": "false"
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`240101` | Invalid client credentials|  


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*