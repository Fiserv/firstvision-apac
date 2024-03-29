# Get Access Token

This API is used to get access token to authenticate and trigger other API's available. If token is expired then user have to regenerate access token again.

## Endpoint

`POST /v1/api/oauth/token`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "grant_type": "client_credentials",
  "scope": "all",
  "client_id": "vision-api-user",
  "client_secret": "abcdefghizklmnopponommnshfghzxxs"
}
```

<!--
type: tab
-->

```json
{
"access_token": "eyJhbGciOiJSUzI1NiJ9.eyJzY29wZSI6ImVkaXQiLCJjbGllbnRfaWQiOiJQT0NfTkFCX0RldiIsImZpcnN0VmlzaW9uSWQiOiIwMDAwMEFVTkFCIiwiZXhwIjoxNzUwMzkyMDAwfQ.uWiSQfLLzfDYuSmPwmLa1fVx6Vyw8Rtphv49uo_2EbfoJYzppHNscar8NWNEp4sXHdxbrEmftu_JJ3oTLD8AtbNgQh9ej8lUEvfA8vbYM3ucXuOC1NWxZPD7tDiwQ6kLypsYgbOhBMQ_U7Icobbh2I9o1Zit8F9xT7J70e3ZLJqtqTWC1WDd0WmOG672KpU_tc2eMtUvLYqrMKjRr2KuD-e73fc27zdYpeL9GElVlo1WKbrHOvsdolr92mvhHBf_etnQ5Pb_X_x533-DiT1piCkjBTqZqgd6cdV2ItdPVAz8CfwmjS6TJR95B3Ys9Xp3tdI5UwP3NmkaYRqP5_R02Q",
"token_type": "Bearer",
"expires_in": 7199
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
      "Invalid client credentials, scope or grant_type"
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
| `scope` | Payload | *string* | 50 | Limit the amount of access that is granted to an access token (accounts, auth, cards, customers, loans, loyalty, misc, products, users, bnpl, all). |
| `grant_type` | Payload | *string* | 50 | It refers to the way an application gets an access token. |
| `client_id` | Payload | *string* | 50 | An identifier associated with an application that assists with client. |
| `client_secret` | Payload | *string* | 100 | a secret known only to your Vision10 API application and the authorization server. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
|`240101` | Invalid client credentials, scope or grant_type |  


*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
