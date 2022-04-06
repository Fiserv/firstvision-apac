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
| `customerServiceBusinessUnit` | payload | *number* | 3 | Customer Service Business Unit of representative. | 
| `businessUnitPrivilegeId` | Payload | *string* | 8 | Name that identifies an existing organization privilege group assigned to this User Security Sign-on record. . | 
| `servicePrivilegeGroupId` | Payload | *string* | 8 | Name that identifies an existing service privilege group assigned to this User Security Sign-on record.. | 

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
| `V5ED0330SV` | Card - Invalid  Reissue-deliv-option |        
| `V5ED0331SV` | Card - Invalid  Issue-deliv-option | 
| `V5ED0010SF` | Update Request - Record not found | 


