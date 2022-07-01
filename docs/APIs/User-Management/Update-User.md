# Update User

This service is used to update security sign-on records like user service privileged record etc.

## Endpoint

`PUT /v1/users/updateUser`

## Payload Example

### Request Payload

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

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/users/updateUser).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientId` | Payload | *number* | 5 | Identification number, referred to as Client ID, assigned to your institution by the processor. | 
| `name` | Payload | *string* | 15 | Sign-on name that the person assigned this User Security Signon record will use to sign on to the system. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

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
  "errorCode": "V5ED0330SV",
  "errorMessage": "Card - Invalid  Reissue-deliv-option"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF4001SE` | Security record selected cannot be viewed by the signed-on user | 
| `VMSF4001ED` | Client is invalid | 
| `VMSF4001SF` | Error in call to subroutine wsorule1 |  
| `VMSF4002SA` | Client name should not be spaces |  
| `VMSF4005EH` | Security record selected cannot be maint by the signed-on user |  
| `VMSF4003EA` | User record must be reactivated before any changes can be made |  
| `VMSF0107EA` | Security expiration date is invalid |  
| `VMSF0107EB` | Field maint not allowed for processor admin |  
| `VMSF0106EA` | Date-to-activate cannot be zeros |
| `VMSF0111EB` | Screen privilege group is invalid |
| `VMSF0111EC` | Screen privilege group does not exist |
| `VMSF0111ED` | Screen privilege type does not conform to this user type |
| `VMSF0111EE` | Restriction group cannot be assigned to a user sign on |
| `VMSF0111EF` | Only approver be assigned to verification scrn privge grp |
| `VMSF0112EA` | Org privilege group is invalid |
| `VMSF0112EB` | Org privilege group does not exist |
| `VMSF0112EC` | Org privilege record is not active |
| `VMSF0112ED` | Org privilege type does not conform to this user type | 
| `VMSF0112EE` | Field maint not allowed for processor admin |
| `VMSF4013EB` | Exclude not allowed when role based option is active | 
| `VMSF4013EC` | Invalid screen include/exclude selection |
| `VMSF4013ED` | Duplicate selection |
| `VMSF4026EA` | Field maint not allowed for processor admin |
| `VMSF4026EC` | Wilcard not allowed in screen selection for user type 5 |
| `VMSF4026ED` | The screen restriction group has not been defined |
| `VMSF4026EF` | Invlaid screen/wildcard selection |
| `VMSF4026EH` | Value may not be added to a signon record with dual value of 2 |
| `VMSF4027EA` | Field maint not allowed for processor admin |
| `VMSF4027EC` | Invalid page/wildcard selection |
| `VMSF4027EE` | Invalid include/exclude and screen/page selection |
| `VMSF4023EA` | Occur 3 14 15 16 18 and 23-30 - reserved for future use |
| `VMSF4023EC` | Invalid user code |
| `VMSF4024EB` | Occur 3 14 15 16 18 and 23-30 - reserved for future use |
| `VMSF4024EC` | Invalid field security code |
| `VMSF0303EB` | Valid entry requires entry in incl/excl name and version fields  | 
| `VMSF0303EC` | No service/version selection to include exclude or delete |
| `VMSF0303ED` | Service/version duplicate selection |
| `VMSF0303ED` | Field maint not allowed for processor admin |
| `VMSF0304EA` | Service/version does not exist- please correct or remove it |      
| `VMSF0304EB` | Service/version is universal & cannot be defined as an override | 
| `VMSF0304EC` | Service/version entered is not allowed |
| `VMSF0304ED` | Field maint not allowed for processor admin |
| `VMSF0304EE` | Valid entry requires entry in incl/excl name and version fields |  
| `VMSF0302EA` | Exclude is not allowed when role-based option is active |          
| `VMSF0302EB` | Invalid selection -use i=include e=exclude or d=delete |           
| `VMSF0302ED` | Field maint not allowed for processor admin |
| `VMSF0301EA` | Service privilege group is required on an add |
| `VMSF0301EB` | Service privilege group is invalid |                               
| `VMSF0301EC` | Service privilege group does not exist |                           
| `VMSF0301ED` | Service privilege type does not conform to this user type |        
| `VMSF0301EE` | A restriction group cannot be applied to a signon |                
| `VMSF0301EF` | Service restriction group is not yet defined-see your admin |      
| `VMSF0301EG` | Clients service restriction grp has severe errors-please correct |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](..docs/?path=docs/common-error-codes.md).*