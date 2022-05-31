# Add User

This service is used to add new security sign-on entity. This newly created entity determine the person’s access rights on the system.
Sign-on entity must be setup and active for each person authorized to access the system. 

*More than one person cannot sign on to the system using the same sign-on entity. A single person cannot sign on using the same sign-on entity at multiple terminals at the same time.*

## Endpoint

`POST /v1/users/boardUser`

## Payload Example

### Request Payload

```json

{
  "clientId": 1,
  "name": "NABTEST25",
  "activationDate": "27/02/2022",
  "signonExpiryDate": "31/12/2025",
  "operatorId": "ABC",
  "customerServiceBusinessUnit": 100,
  "businessUnitPrivilegeId": "CLTUSER",
  "servicePrivilegeGroupId": "CLTUSER",
  "supervisorId": " ",
  "sourceGroupType": "2",
  "businessUnitIncludeExcludeFlagReq": {
    "businessUnitIncludeExcludeFlag1Req": {
      "inclusionExclusionFlag1": " ",
      "businessUnit1": " "
    },
    "businessUnitIncludeExcludeFlag2Req": {
      "inclusionExclusionFlag2": " ",
      "businessUnit2": " "
    },
    "businessUnitIncludeExcludeFlag3Req": {
      "inclusionExclusionFlag3": " ",
      "businessUnit3": " "
    },
    "businessUnitIncludeExcludeFlag4Req": {
      "inclusionExclusionFlag4": " ",
      "businessUnit4": " "
    },
    "businessUnitIncludeExcludeFlag5Req": {
      "inclusionExclusionFlag5": " ",
      "businessUnit5": " "
    },
    "businessUnitIncludeExcludeFlag6Req": {
      "inclusionExclusionFlag6": " ",
      "businessUnit6": " "
    },
    "businessUnitIncludeExcludeFlag7Req": {
      "inclusionExclusionFlag7": " ",
      "businessUnit7": " "
    },
    "businessUnitIncludeExcludeFlag8Req": {
      "inclusionExclusionFlag8": " ",
      "businessUnit8": " "
    },
    "businessUnitIncludeExcludeFlag9Req": {
      "inclusionExclusionFlag9": " ",
      "businessUnit9": " "
    },
    "businessUnitIncludeExcludeFlag10Req": {
      "inclusionExclusionFlag10": " ",
      "businessUnit10": " "
    }
  },
  "userApplicationAccessReq": {
    "ctryCurrencyCatCodesReq": {
      "userCode1": " ",
      "fieldSecurityCode1": " "
    },
    "businessMessagingReq": {
      "userCode2": " ",
      "fieldSecurityCode2": " "
    },
    "futureUse03Req": {
      "userCode3": " ",
      "fieldSecurityCode3": " "
    },
    "exceptionProcessingReq": {
      "userCode4": " ",
      "fieldSecurityCode4": " "
    },
    "accountManagementReq": {
      "userCode5": " ",
      "fieldSecurityCode5": " "
    },
    "collectionManagementReq": {
      "userCode6": " ",
      "fieldSecurityCode6": " "
    },
    "authorizationsReq": {
      "userCode7": " ",
      "fieldSecurityCode7": " "
    },
    "customerServiceReq": {
      "userCode8": " ",
      "fieldSecurityCode8": " "
    },
    "remoteInterfaceReq": {
      "userCode9": " ",
      "fieldSecurityCode9": " "
    },
    "commercialCardReq": {
      "userCode10": " ",
      "fieldSecurityCode10": " "
    },
    "OfferManagementReq": {
      "userCode11": " ",
      "fieldSecurityCode11": " "
    },
    "merchantSettlementReq": {
      "userCode12": " ",
      "fieldSecurityCode12": " "
    },
    "\tapplicationProcessingReq": {
      "userCode13": " ",
      "fieldSecurityCode13": " "
    },
    "embScriptingSystemReq": {
      "userCode14": " ",
      "fieldSecurityCode14": " "
    },
    "keyManagementSystemReq": {
      "userCode15": " ",
      "fieldSecurityCode15": " "
    },
    "futureUse16Req": {
      "userCode16": " ",
      "fieldSecurityCode16": " "
    },
    "letterRequestsReq": {
      "userCode17": " ",
      "fieldSecurityCode17": " "
    },
    "futureUse18Req": {
      "userCode18": " ",
      "fieldSecurityCode18": " "
    },
    "internationalLanguageReq": {
      "userCode19": " ",
      "fieldSecurityCode19": " "
    },
    "rewardManagementReq": {
      "userCode20": " ",
      "fieldSecurityCode20": " "
    },
    "clientSupportReq": {
      "userCode21": " ",
      "fieldSecurityCode21": " "
    },
    "securityReq": {
      "userCode22": " ",
      "fieldSecurityCode22": " "
    },
    "connectionManagerReq": {
      "userCode23": " ",
      "fieldSecurityCode23": " "
    },
    "posDeviceManagementReq": {
      "userCode24": " ",
      "fieldSecurityCode24": " "
    },
    "customerCommunicationManagementReq": {
      "userCode25": " ",
      "fieldSecurityCode25": " "
    },
    "decisionEngineSystemReq": {
      "userCode26": " ",
      "fieldSecurityCode26": " "
    },
    "futureUse27Req": {
      "userCode27": " ",
      "fieldSecurityCode27": " "
    },
    "futureUse28Req": {
      "userCode28": " ",
      "fieldSecurityCode28": " "
    },
    "transactionManagementReq": {
      "userCode29": " ",
      "fieldSecurityCode29": " "
    },
    "futureUse30Req": {
      "userCode30": " ",
      "fieldSecurityCode30": " "
    }
  },
  "userServicePrivilegeReq": {
    "userServicePrivilege1Req": {
      "serviceInclusionExclusionFlag1": " ",
      "serviceName1": " ",
      "serviceVersion1": " "
    },
    "userServicePrivilege2Req": {
      "serviceInclusionExclusionFlag2": " ",
      "serviceName2": " ",
      "serviceVersion2": " "
    },
    "userServicePrivilege3Req": {
      "serviceInclusionExclusionFlag3": " ",
      "serviceName3": " ",
      "serviceVersion3": " "
    },
    "userServicePrivilege4Req": {
      "serviceInclusionExclusionFlag4": " ",
      "serviceName4": " ",
      "serviceVersion4": " "
    },
    "userServicePrivilege5Req": {
      "serviceInclusionExclusionFlag5": " ",
      "serviceName5": " ",
      "serviceVersion5": " "
    },
    "userServicePrivilege6Req": {
      "serviceInclusionExclusionFlag6": " ",
      "serviceName6": " ",
      "serviceVersion6": " "
    },
    "userServicePrivilege7Req": {
      "serviceInclusionExclusionFlag7": " ",
      "serviceName7": " ",
      "serviceVersion7": " "
    },
    "userServicePrivilege8Req": {
      "serviceInclusionExclusionFlag8": " ",
      "serviceName8": " ",
      "serviceVersion8": " "
    },
    "userServicePrivilege9Req": {
      "serviceInclusionExclusionFlag9": " ",
      "serviceName9": " ",
      "serviceVersion9": " "
    },
    "userServicePrivilege10Req": {
      "serviceInclusionExclusionFlag10": " ",
      "serviceName10": " ",
      "serviceVersion10": " "
    }
  }
}

``` 

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/users/boardUser).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientID` | Payload | *string* | 05 | Identification number, referred to as Client ID, assigned to your institution by the processor. |
| `name` | Payload | *string* | 15 | Sign-on name that the person assigned this User Security Signon entity will use to sign on to the  system. |
| `activationDate` | Payload | *date* | 10 | Activation date of the User Security Sign-on entity. |
| `operatorID` | Payload | *string* | 03 | Representative ID of of an operator. |
| `customerServiceBusinessUnit` | Payload | *number* | 03 | Customer business organization unit. |
| `businessPreviligeID` | Payload | *number* | 03 | Name that identifies an existing organization privilege group assigned to this User Security Sign-on entity. |
| `servicePrivilegeGroup` | Payload | *number* | 03 |  Name that identifies an existing service privilege group assigned to this User Security Sign-on entity. |
| `signonExpiryDate` | Payload | *date* | 10 |  Expiration date of the User Security Sign-on entity. The default value is zeros. |

### Successful Response Payload

```json
{}

```

### Error Response Payload

```json
{
   errorCode" :  VMSF4001EB" ,
   errorMessage" : Client is invalid"   
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF4001EB`  |  Client is invalid | 
| `VMSF4002SA`  |  Client name should not be spaces |
| `VMSF0107EA`  |  Security expiration date is invalid |
| `VMSF0106EA`  |  Date-To-Activate cannot be zeros | 
| `VMSF0112EA`  |  Org privilege group is invalid |
| `VMSF0112EB`  |  Org privilege group does not exist | 
| `VMSF0112EC`  |  Privilege record is not active |
| `VMSF0112ED`  |  Org privilege type does not confirm to this user type |
| `VMSF0150EA`  |  Source group occurrence is not active |
| `VMSF0108EC`  |  Oper ID in use by another user - Please enter another oper ID | 
| `VMSF0109EA`  |  CS Rep Org number is invalid |
| `VMSF0116EA`  |  Invalid org include/exclude selection |
| `VMSF0116EB`  |  Invalid include/exclude and org selection | 
| `VMSF0116EC`  |  Duplicate org selection |
| `VMSF4024EC`  |  Invalid field security code | 
| `VMSF0302EB`  |  Invalid selection - Use I=Include E=Exclude Or D=Delete |
| `VMSF0303EB`  |  Valid entry requires entry in Incl/Excl name and version fields |
| `VMSF0303EC`  |  No service/version selection to include exclude or delete |
| `VMSF0304EA`  |  Service/version does not exist- Please correct or remove it | 
| `VMSF0304EB`  |  Service/version is universal & cannot be defined as an override |
| `VMSF0304EC`  |  Service/version entered is not allowed |
| `VMSF0304EE`  |  Valid entry requires entry in Incl/Excl name and version fields |