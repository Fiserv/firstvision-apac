# Update User profile

This service is used to update security sign-on records like business unit include/exclude flags, User application access record, user service privileged record etc.

## Endpoint

`PUT /v1/users/updateUserProfile`

## Payload Example

### Request Payload

```json

{
  "clientId": 1,
  "name": "NABTESKL6",
  "type": "5",
  "servicePrivilegeGroupId": "",
  "status": "1",
  "signonExpiryDate": "",
  "dateToActivate": "",
  "businessUnitPrivilegeId": "",
  "supervisorId": "",
  "customerServiceBusinessUnit": 100,
  "businessUnitIncludeExcludeFlagReq": {
    "businessUnitIncludeExcludeFlag1Req": {
      "inclusionExclusionFlag1": "",
      "businessUnit1": ""
    },
    "businessUnitIncludeExcludeFlag2Req": {
      "inclusionExclusionFlag2": "",
      "businessUnit2": ""
    },
    "businessUnitIncludeExcludeFlag3Req": {
      "inclusionExclusionFlag3": "",
      "businessUnit3": ""
    },
    "businessUnitIncludeExcludeFlag4Req": {
      "inclusionExclusionFlag4": "",
      "businessUnit4": ""
    },
    "businessUnitIncludeExcludeFlag5Req": {
      "inclusionExclusionFlag5": "",
      "businessUnit5": ""
    },
    "businessUnitIncludeExcludeFlag6Req": {
      "inclusionExclusionFlag6": "",
      "businessUnit6": ""
    },
    "businessUnitIncludeExcludeFlag7Req": {
      "inclusionExclusionFlag7": "",
      "businessUnit7": ""
    },
    "businessUnitIncludeExcludeFlag8Req": {
      "inclusionExclusionFlag8": "",
      "businessUnit8": ""
    },
    "businessUnitIncludeExcludeFlag9Req": {
      "inclusionExclusionFlag9": "",
      "businessUnit9": ""
    },
    "businessUnitIncludeExcludeFlag10Req": {
      "inclusionExclusionFlag10": "",
      "businessUnit10": ""
    }
  },
  "userApplicationAccessReq": {
    "ctryCurrencyCatCodesReq": {
      "userCode1": "",
      "fieldSecurityCode1": ""
    },
    "businessMessagingReq": {
      "userCode2": "",
      "fieldSecurityCode2": ""
    },
    "futureUse03Req": {
      "userCode3": "",
      "fieldSecurityCode3": ""
    },
    "exceptionProcessingReq": {
      "userCode4": "",
      "fieldSecurityCode4": ""
    },
    "accountManagementReq": {
      "userCode5": "",
      "fieldSecurityCode5": ""
    },
    "collectionManagementReq": {
      "userCode6": "",
      "fieldSecurityCode6": ""
    },
    "authorizationsReq": {
      "userCode7": "",
      "fieldSecurityCode7": ""
    },
    "customerServiceReq": {
      "userCode8": "",
      "fieldSecurityCode8": ""
    },
    "remoteInterfaceReq": {
      "userCode9": "",
      "fieldSecurityCode9": ""
    },
    "commercialCardReq": {
      "userCode10": "",
      "fieldSecurityCode10": ""
    },
    "OfferManagementReq": {
      "userCode11": "",
      "fieldSecurityCode11": ""
    },
    "merchantSettlementReq": {
      "userCode12": "",
      "fieldSecurityCode12": ""
    },
    "applicationProcessingReq": {
      "userCode13": "",
      "fieldSecurityCode13": ""
    },
    "embScriptingSystemReq": {
      "userCode14": "",
      "fieldSecurityCode14": ""
    },
    "keyManagementSystemReq": {
      "userCode15": "",
      "fieldSecurityCode15": ""
    },
    "futureUse16Req": {
      "userCode16": "",
      "fieldSecurityCode16": ""
    },
    "letterRequestsReq": {
      "userCode17": "",
      "fieldSecurityCode17": ""
    },
    "futureUse18Req": {
      "userCode18": "",
      "fieldSecurityCode18": ""
    },
    "internationalLanguageReq": {
      "userCode19": "",
      "fieldSecurityCode19": ""
    },
    "rewardManagementReq": {
      "userCode20": "",
      "fieldSecurityCode20": ""
    },
    "clientSupportReq": {
      "userCode21": "",
      "fieldSecurityCode21": ""
    },
    "securityReq": {
      "userCode22": "",
      "fieldSecurityCode22": ""
    },
    "connectionManagerReq": {
      "userCode23": "",
      "fieldSecurityCode23": ""
    },
    "posDeviceManagementReq": {
      "userCode24": "",
      "fieldSecurityCode24": ""
    },
    "customerCommunicationManagementReq": {
      "userCode25": "",
      "fieldSecurityCode25": ""
    },
    "decisionEngineSystemReq": {
      "userCode26": "",
      "fieldSecurityCode26": ""
    },
    "futureUse27Req": {
      "userCode27": "",
      "fieldSecurityCode27": ""
    },
    "futureUse28Req": {
      "userCode28": "",
      "fieldSecurityCode28": ""
    },
    "transactionManagementReq": {
      "userCode29": "",
      "fieldSecurityCode29": ""
    },
    "futureUse30Req": {
      "userCode30": "",
      "fieldSecurityCode30": ""
    }
  },
  "userServicePrivilegeReq": {
    "userServicePrivilege1Req": {
      "serviceInclusionExclusionflag1": "",
      "serviceName1": "",
      "serviceVersion1": ""
    },
    "userServicePrivilege2Req": {
      "serviceInclusionExclusionflag2": "",
      "serviceName2": "",
      "serviceVersion2": ""
    },
    "userServicePrivilege3Req": {
      "serviceInclusionExclusionflag3": "",
      "serviceName3": "",
      "serviceVersion3": ""
    },
    "userServicePrivilege4Req": {
      "serviceInclusionExclusionflag4": "",
      "serviceName4": "",
      "serviceVersion4": ""
    },
    "userServicePrivilege5Req": {
      "serviceInclusionExclusionflag5": "",
      "serviceName5": "",
      "serviceVersion5": ""
    },
    "userServicePrivilege6Req": {
      "serviceInclusionExclusionflag6": "",
      "serviceName6": "",
      "serviceVersion6": ""
    },
    "userServicePrivilege7Req": {
      "serviceInclusionExclusionflag7": "",
      "serviceName7": "",
      "serviceVersion7": ""
    },
    "userServicePrivilege8Req": {
      "serviceInclusionExclusionflag8": "",
      "serviceName8": "",
      "serviceVersion8": ""
    },
    "userServicePrivilege9Req": {
      "serviceInclusionExclusionflag9": "",
      "serviceName9": "",
      "serviceVersion9": ""
    },
    "userServicePrivilege10Req": {
      "serviceInclusionExclusionflag10": "",
      "serviceName10": "",
      "serviceVersion10": ""
    }
  }
}
```

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/users/updateUserProfile).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientId` | Payload | *number* | 5 | TIdentification number, referred to as Client ID, assigned to your institution by the processor. | 
| `name` | Payload | *string* | 15 | Sign-on name that the person assigned this User Security Signon record will use to sign on to the system. | 

*In addition to the above mentioned minimum field, one of the request payload variable is required.*

### Successful Response Payload

```json
{
  "clientId": 1,
  "name": "NABTESKL6",
  "type": "5",
  "servicePrivilegeGroupId": "",
  "status": "1",
  "signonExpiryDate": "",
  "dateToActivate": "",
  "businessUnitPrivilegeId": "",
  "supervisorId": "",
  "customerServiceBusinessUnit": 100,
  "businessUnitIncludeExcludeFlagRes": {
    "businessUnitIncludeExcludeFlag1Res": {
      "inclusionExclusionFlag1": "",
      "businessUnit1": ""
    },
    "businessUnitIncludeExcludeFlag2Res": {
      "inclusionExclusionFlag2": "",
      "businessUnit2": ""
    },
    "businessUnitIncludeExcludeFlag3Res": {
      "inclusionExclusionFlag3": "",
      "businessUnit3": ""
    },
    "businessUnitIncludeExcludeFlag4Res": {
      "inclusionExclusionFlag4": "",
      "businessUnit4": ""
    },
    "businessUnitIncludeExcludeFlag5Res": {
      "inclusionExclusionFlag5": "",
      "businessUnit5": ""
    },
    "businessUnitIncludeExcludeFlag6Res": {
      "inclusionExclusionFlag6": "",
      "businessUnit6": ""
    },
    "businessUnitIncludeExcludeFlag7Res": {
      "inclusionExclusionFlag7": "",
      "businessUnit7": ""
    },
    "businessUnitIncludeExcludeFlag8Res": {
      "inclusionExclusionFlag8": "",
      "businessUnit8": ""
    },
    "businessUnitIncludeExcludeFlag9Res": {
      "inclusionExclusionFlag9": "",
      "businessUnit9": ""
    },
    "businessUnitIncludeExcludeFlag10Res": {
      "inclusionExclusionFlag10": "",
      "businessUnit10": ""
    }
  },
  "userApplicationAccessRes": {
    "ctryCurrencyCatCodesRes": {
      "userCode1": "",
      "fieldSecurityCode1": ""
    },
    "businessMessagingRes": {
      "userCode2": "",
      "fieldSecurityCode2": ""
    },
    "futureUse03Res": {
      "userCode3": "",
      "fieldSecurityCode3": ""
    },
    "exceptionProcessingRes": {
      "userCode4": "",
      "fieldSecurityCode4": ""
    },
    "accountManagementRes": {
      "userCode5": "",
      "fieldSecurityCode5": ""
    },
    "collectionManagementRes": {
      "userCode6": "",
      "fieldSecurityCode6": ""
    },
    "authorizationsRes": {
      "userCode7": "",
      "fieldSecurityCode7": ""
    },
    "customerServiceRes": {
      "userCode8": "",
      "fieldSecurityCode8": ""
    },
    "remoteInterfaceRes": {
      "userCode9": "",
      "fieldSecurityCode9": ""
    },
    "commercialCardRes": {
      "userCode10": "",
      "fieldSecurityCode10": ""
    },
    "OfferManagementRes": {
      "userCode11": "",
      "fieldSecurityCode11": ""
    },
    "merchantSettlementRes": {
      "userCode12": "",
      "fieldSecurityCode12": ""
    },
    "applicationProcessingRes": {
      "userCode13": "",
      "fieldSecurityCode13": ""
    },
    "embScriptingSystemRes": {
      "userCode14": "",
      "fieldSecurityCode14": ""
    },
    "keyManagementSystemRes": {
      "userCode15": "",
      "fieldSecurityCode15": ""
    },
    "futureUse16Res": {
      "userCode16": "",
      "fieldSecurityCode16": ""
    },
    "letterRequestsRes": {
      "userCode17": "",
      "fieldSecurityCode17": ""
    },
    "futureUse18Res": {
      "userCode18": "",
      "fieldSecurityCode18": ""
    },
    "internationalLanguageRes": {
      "userCode19": "",
      "fieldSecurityCode19": ""
    },
    "rewardManagementRes": {
      "userCode20": "",
      "fieldSecurityCode20": ""
    },
    "clientSupportRes": {
      "userCode21": "",
      "fieldSecurityCode21": ""
    },
    "securityRes": {
      "userCode22": "",
      "fieldSecurityCode22": ""
    },
    "connectionManagerRes": {
      "userCode23": "",
      "fieldSecurityCode23": ""
    },
    "posDeviceManagementRes": {
      "userCode24": "",
      "fieldSecurityCode24": ""
    },
    "customerCommunicationManagementRes": {
      "userCode25": "",
      "fieldSecurityCode25": ""
    },
    "decisionEngineSystemRes": {
      "userCode26": "",
      "fieldSecurityCode26": ""
    },
    "futureUse27Res": {
      "userCode27": "",
      "fieldSecurityCode27": ""
    },
    "futureUse28Res": {
      "userCode28": "",
      "fieldSecurityCode28": ""
    },
    "transactionManagementRes": {
      "userCode29": "",
      "fieldSecurityCode29": ""
    },
    "futureUse30Res": {
      "userCode30": "",
      "fieldSecurityCode30": ""
    }
  },
  "userServicePrivilegeRes": {
    "userServicePrivilege1Res": {
      "serviceInclusionExclusionflag1": "",
      "serviceName1": "",
      "serviceVersion1": ""
    },
    "userServicePrivilege2Res": {
      "serviceInclusionExclusionflag2": "",
      "serviceName2": "",
      "serviceVersion2": ""
    },
    "userServicePrivilege3Res": {
      "serviceInclusionExclusionflag3": "",
      "serviceName3": "",
      "serviceVersion3": ""
    },
    "userServicePrivilege4Res": {
      "serviceInclusionExclusionflag4": "",
      "serviceName4": "",
      "serviceVersion4": ""
    },
    "userServicePrivilege5Res": {
      "serviceInclusionExclusionflag5": "",
      "serviceName5": "",
      "serviceVersion5": ""
    },
    "userServicePrivilege6Res": {
      "serviceInclusionExclusionflag6": "",
      "serviceName6": "",
      "serviceVersion6": ""
    },
    "userServicePrivilege7Res": {
      "serviceInclusionExclusionflag7": "",
      "serviceName7": "",
      "serviceVersion7": ""
    },
    "userServicePrivilege8Res": {
      "serviceInclusionExclusionflag8": "",
      "serviceName8": "",
      "serviceVersion8": ""
    },
    "userServicePrivilege9Res": {
      "serviceInclusionExclusionflag9": "",
      "serviceName9": "",
      "serviceVersion9": ""
    },
    "userServicePrivilege10Res": {
      "serviceInclusionExclusionflag10": "",
      "serviceName10": "",
      "serviceVersion10": ""
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


