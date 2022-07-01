# Get Access Token

This service is used to get Access Token to authenticate and trigger the API's available. If token is expired then user have to regenerate access token again using this service.

## Endpoint

`GET /v1/getAccessToken`

## Payload Example

### Request Payload

```json
{scope: ["firstvision.accountmanagement.read"]}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/getAccessToken).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `scope` | Path Variable | *string* | 50 | Scope for which the token has been requested. |

### Successful Response Payload

```json
{
"access_token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImVkaXQiLCJjbGllbnRfaWQiOiJQT0NfTkFCX0RldiIsImZpcnN0VmlzaW9uSWQiOiIwMDAwMEFVTkFCIiwiZXhwIjoxNzUwMzkyMDAwfQ.uWiSQfLLzfDYuSmPwmLa1fVx6Vyw8Rtphv49uo_2EbfoJYzppHNscar8NWNEp4sXHdxbrEmftu_JJ3oTLD8AtbNgQh9ej8lUEvfA8vbYM3ucXuOC1NWxZPD7tDiwQ6kLypsYgbOhBMQ_U7Icobbh2I9o1Zit8F9xT7J70e3ZLJqtqTWC1WDd0WmOG672KpU_tc2eMtUvLYqrMKjRr2KuD-e73fc27zdYpeL9GElVlo1WKbrHOvsdolr92mvhHBf_etnQ5Pb_X_x533-DiT1piCkjBTqZqgd6cdV2ItdPVAz8CfwmjS6TJR95B3Ys9Xp3tdI5UwP3NmkaYRqP5_R02Q",
"expires_in": 1750392000,
"token_type": "Bearer"
}
```

### Error Response Payload

```json
{
  "errorCode": "AGT415UMT",
  "errorMessage": "Content type is not provided"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`AGT415UMT` |Content type is not provided|  
|`AGT415UMT` |Allowed content type for this client is application/json|
|`AGT415UMT` |Allowed content type for this client is octet-stream|
|`AGT400BR` |Payload is not valid|
|`AGT400BR` |Authorization header is missing|
|`AGT401UA` |Pass expired token in customer search API and get proper error message from gateway|
|`AGT401UA` |Access token is missing in request|

