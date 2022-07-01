# Inquire User

This service is used to inquire security sign-on deta like business unit include/exclude flags, User application access record, user service privileged record etc.

## Endpoint

`GET /v1/users/inquireUser`

## Payload Example

### Request Payload

Request Payload

>Should be empty.  
>
***The client id and name should be sent as query variable.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/users/inquireUser).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientId` | Query Parameter | *number* | 5 | Identification number, referred to as Client ID, assigned to your institution by the processor. | 
| `name` | Query Parameter | *string* | 15 | Sign-on name that the person assigned this User Security Signon record will use to sign on to the system. | 


### Successful Response Payload

```json

{
  "clientId": 1,
  "name": "NABTEST25",
  "securityType": "5",
  "servicePrivilegeGroupId": "",
  "status": "1",
  "signonExpiryDate": "",
  "activationDate": "",
  "businessUnitPrivilegeId": "",
  "supervisorId": " ",
  "customerServiceBusinessUnit": 100,
  "userServicePrivilege": {
    "userServicePrivilege1": {
      "serviceInclusionExclusionFlag1": " ",
      "serviceName1": " ",
      "serviceVersion1": " "
    },
    "userServicePrivilege2": {
      "serviceInclusionExclusionFlag2": " ",
      "serviceName2": " ",
      "serviceVersion2": " "
    },
    "userServicePrivilege3": {
      "serviceInclusionExclusionFlag3": " ",
      "serviceName3": " ",
      "serviceVersion3": " "
    },
    "userServicePrivilege4": {
      "serviceInclusionExclusionFlag4": " ",
      "serviceName4": " ",
      "serviceVersion4": " "
    },
    "userServicePrivilege5": {
      "serviceInclusionExclusionFlag5": " ",
      "serviceName5": " ",
      "serviceVersion5": " "
    },
    "userServicePrivilege6": {
      "serviceInclusionExclusionFlag6": " ",
      "serviceName6": " ",
      "serviceVersion6": " "
    },
    "userServicePrivilege7": {
      "serviceInclusionExclusionFlag7": " ",
      "serviceName7": " ",
      "serviceVersion7": " "
    },
    "userServicePrivilege8": {
      "serviceInclusionExclusionFlag8": " ",
      "serviceName8": " ",
      "serviceVersion8": " "
    },
    "userServicePrivilege9": {
      "serviceInclusionExclusionFlag9": " ",
      "serviceName9": " ",
      "serviceVersion9": " "
    },
    "userServicePrivilege10": {
      "serviceInclusionExclusionFlag10": " ",
      "serviceName10": " ",
      "serviceVersion10": " "
    }
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "VMSF0011SF",
  "errorMessage": "Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF0001SA` | Invalid request for this user security | 
| `VMSF0011SF` | Record not found | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*