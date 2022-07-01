# Signon User

This service is used to sign-on to the system with the given user ID and password. This service provides the unique context number every time user has signed-in.
  
## Endpoint

`POST /v1/users/signOn`

## Payload Example

### Request Payload

```json
{
  "securityName": "00001NABTEST5",
  "secret": "A5360008B9633FECB5759DBC0BDEECAF795CDC1C60CE666C7460EF7A1421C91ADD8DAFB4A75F5E307CE1B885BD548E2AB0FB1EB7B21A91C84E1F5D48137F164EA48ED5B10FF412DE41F923108580E7DC1DF28F29D3BEB516EB901CF52F437C21F325D0F1FB6C3085B2741EFA661B81F484994539AC4E469088476E5327F1FCC8457CADBE8AFA0CDCC31B670518E7BF4B9E486F1818C2370134F9EE7B524BA4EBAA8C71BD649B04AE450BBC8CE538973C4A6DE40F8AD86E5CED1E0CDE09CB076EF31289227E1D3F4FD01270B66D625D16747B814F374F51D13A48E37745D61935EAE393DE8511A7AC3FFA5486DE38E127B84C2C206AB75F59AF65681C03E1B9E4"
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/users/signOn).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `securityName` | Payload | *string* | 128 | Sign-on name assigned to the person signing on to the system. |
| `secret` | Payload | *string* | 512 | Encrypted Password for signing on to the system. | 

### Successful Response Payload

```json

{
  "securityContext": "00007692720915663"
}

```

### Error Response Payload

```json
{
  "errorCode": "VMES0025EF",
  "errorMessage": "Client/Name Or password is invalid - Please Retry"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMES0025EF` | Client/Name or password is invalid - Please retry |   

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*
