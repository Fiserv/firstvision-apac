# User Signon

This service is used to sign-on to the system with the given user ID and password. This service provides the unique context number every time user has signed-in.
  
## Endpoint

`POST /v1/users/signOn`

## Payload Example

### Request Payload

```json
{
"securityName": "00001NABTEST5",
"secret":   "A3CDCAE523A132FFAE3800958AC12AB7B62E0DA876C4C91A10C9AC4FF7DF18BF6940F5AEAF33BA381522594D03108CB7A8B46FF39BEE944A98DD26201F36ACFA71D15A875947741961188B661123BF507AB6A9D5E82BA5083D0DB98F54E6D857D9A5B4A48D2750A81A405563B656352230D9613D80F3A362867C1C59BBA09FFED3669DE30905631A4DD9DF68CA47F6E58A0987CCDECBEBD72229F8312684F7E3A5DBDB7E1F99690B7AD44A645EBA0D3BC5CD26F411E6FBED3F430BD2BA372118D934350A7BAC7DBD18BFDB54B3DEFCBC24A8C75768C3C9C766FE75AD3032BAFED6F886F02692DD1C38FF6088088069B281CFF12F745606F758932E83301878CA"
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
  "securityContext": "00005272985347389"
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
