# Get Access Token

This service is used to get Access Token to authenticate and trigger the API's available. If token is expired then user have to regenerate access token again using this service.

## Endpoint

`POST /v1/api/oauth/token`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***Scope detail for token sent as Query Parameter.***

<!--
type: tab
-->

```json
{
"access_token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImVkaXQiLCJjbGllbnRfaWQiOiJQT0NfTkFCX0RldiIsImZpcnN0VmlzaW9uSWQiOiIwMDAwMEFVTkFCIiwiZXhwIjoxNzUwMzkyMDAwfQ.uWiSQfLLzfDYuSmPwmLa1fVx6Vyw8Rtphv49uo_2EbfoJYzppHNscar8NWNEp4sXHdxbrEmftu_JJ3oTLD8AtbNgQh9ej8lUEvfA8vbYM3ucXuOC1NWxZPD7tDiwQ6kLypsYgbOhBMQ_U7Icobbh2I9o1Zit8F9xT7J70e3ZLJqtqTWC1WDd0WmOG672KpU_tc2eMtUvLYqrMKjRr2KuD-e73fc27zdYpeL9GElVlo1WKbrHOvsdolr92mvhHBf_etnQ5Pb_X_x533-DiT1piCkjBTqZqgd6cdV2ItdPVAz8CfwmjS6TJR95B3Ys9Xp3tdI5UwP3NmkaYRqP5_R02Q",
"expires_in": 1750392000,
"token_type": "Bearer"
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
    "instance": "/v1/api/oauth/token",
    "invalid-params": [
      "Invalid client credentials or scope"
    ],
    "source": "AGT",
    "status": 401,
    "title": "Unauthorized"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/api/oauth/token).

The below table identifies the required query parameters in the request message.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `scope` | Query Parameter | *string* | 50 | Scope for which the token has been requested. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`240101` | Invalid client credentials or scope|  


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*