# Inquire User

This API is used to fetch generic details like status, expiry date etc. and service privileged details for a given security sign-on details.

## Endpoint

`GET /v1/users/inquireUser`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
***The client id and name should be sent as query variable.***

<!--
type: tab
-->

```json
{
  "activationDate": "24/06/2021",
  "businessUnitPrivilegeId": "CLTUSER",
  "clientId": 1,
  "customerServiceBusinessUnit": 100,
  "name": "NABTEST25",
  "servicePrivilegeGroupId": "CLTUSER",
  "signonExpiryDate": "31/12/2023",
  "status": "1",
  "supervisorId": "",
  "userServicePrivilege01": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege02": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege03": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege04": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege05": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege06": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege07": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege08": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege09": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
  },
  "userServicePrivilege10": {
    "serviceInclusionExclusionFlag": "",
    "serviceName": "",
    "serviceVersion": ""
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
    "instance": "/v1/users/inquireUser",
    "invalid-params": [
      "VMSF0010SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/users/inquireUser).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientId` | Query Parameter | *number* | 5 | Identification number, referred to as Client ID, assigned to your institution by the processor. | 
| `name` | Query Parameter | *string* | 15 | Sign-on name that the person assigned this User Security Signon record will use to sign on to the system. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF0001SA` | Invalid request for this user security | 
| `VMSF0011SF` | Get request - Record not found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*