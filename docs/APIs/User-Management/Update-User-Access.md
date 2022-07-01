# Update User Access

This service is used to update security sign-on data like business unit include/exclude flags and user application access options.

## Endpoint

`PUT /v1/users/access`

## Payload Example

### Request Payload

```json
{
  "clientId": 1,
  "name": "NABTEST25",
  "userApplicationAccess": {
    "ctryCurrencyCatCodes": {
      "userCode1": " ",
      "fieldSecurityCode1": " "
    },
    "businessMessaging": {
      "userCode2": " ",
      "fieldSecurityCode2": " "
    },
    "futureUse03": {
      "userCode3": " ",
      "fieldSecurityCode3": " "
    },
    "exceptionProcessing": {
      "userCode4": " ",
      "fieldSecurityCode4": " "
    },
    "accountManagement": {
      "userCode5": " ",
      "fieldSecurityCode5": " "
    },
    "collectionManagement": {
      "userCode6": " ",
      "fieldSecurityCode6": " "
    },
    "authorizations": {
      "userCode7": " ",
      "fieldSecurityCode7": " "
    },
    "customerService": {
      "userCode8": " ",
      "fieldSecurityCode8": " "
    },
    "remoteInterface": {
      "userCode9": " ",
      "fieldSecurityCode9": " "
    },
    "commercialCard": {
      "userCode10": " ",
      "fieldSecurityCode10": " "
    },
    "OfferManagement": {
      "userCode11": " ",
      "fieldSecurityCode11": " "
    },
    "merchantSettlement": {
      "userCode12": " ",
      "fieldSecurityCode12": " "
    },
    "applicationProcessing": {
      "userCode13": " ",
      "fieldSecurityCode13": " "
    },
    "embScriptingSystem": {
      "userCode14": " ",
      "fieldSecurityCode14": " "
    },
    "keyManagementSystem": {
      "userCode15": " ",
      "fieldSecurityCode15": " "
    },
    "futureUse16": {
      "userCode16": " ",
      "fieldSecurityCode16": " "
    },
    "letterRequests": {
      "userCode17": " ",
      "fieldSecurityCode17": " "
    },
    "futureUse18": {
      "userCode18": " ",
      "fieldSecurityCode18": " "
    },
    "internationalLanguage": {
      "userCode19": " ",
      "fieldSecurityCode19": " "
    },
    "rewardManagement": {
      "userCode20": " ",
      "fieldSecurityCode20": " "
    },
    "clientSupport": {
      "userCode21": " ",
      "fieldSecurityCode21": " "
    },
    "security": {
      "userCode22": " ",
      "fieldSecurityCode22": " "
    },
    "connectionManager": {
      "userCode23": " ",
      "fieldSecurityCode23": " "
    },
    "posDeviceManagement": {
      "userCode24": " ",
      "fieldSecurityCode24": " "
    },
    "customerCommunicationManagement": {
      "userCode25": " ",
      "fieldSecurityCode25": " "
    },
    "decisionEngineSystem": {
      "userCode26": " ",
      "fieldSecurityCode26": " "
    },
    "futureUse27": {
      "userCode27": " ",
      "fieldSecurityCode27": " "
    },
    "futureUse28": {
      "userCode28": " ",
      "fieldSecurityCode28": " "
    },
    "transactionManagement": {
      "userCode29": " ",
      "fieldSecurityCode29": " "
    },
    "futureUse30": {
      "userCode30": " ",
      "fieldSecurityCode30": " "
    }
  },
  "businessUnitIncludeExcludeFlag": {
    "businessUnitIncludeExcludeFlag1": {
      "inclusionExclusionFlag1": " ",
      "businessUnit1": " "
    },
    "businessUnitIncludeExcludeFlag2": {
      "inclusionExclusionFlag2": " ",
      "businessUnit2": " "
    },
    "businessUnitIncludeExcludeFlag3": {
      "inclusionExclusionFlag3": " ",
      "businessUnit3": " "
    },
    "businessUnitIncludeExcludeFlag4": {
      "inclusionExclusionFlag4": " ",
      "businessUnit4": " "
    },
    "businessUnitIncludeExcludeFlag5": {
      "inclusionExclusionFlag5": " ",
      "businessUnit5": " "
    },
    "businessUnitIncludeExcludeFlag6": {
      "inclusionExclusionFlag6": " ",
      "businessUnit6": " "
    },
    "businessUnitIncludeExcludeFlag7": {
      "inclusionExclusionFlag7": " ",
      "businessUnit7": " "
    },
    "businessUnitIncludeExcludeFlag8": {
      "inclusionExclusionFlag8": " ",
      "businessUnit8": " "
    },
    "businessUnitIncludeExcludeFlag9": {
      "inclusionExclusionFlag9": " ",
      "businessUnit9": " "
    },
    "businessUnitIncludeExcludeFlag10": {
      "inclusionExclusionFlag10": " ",
      "businessUnit10": " "
    }
  }
}

```
### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=put&path=/v1/users/access).

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
  "userApplicationAccess": {
    "ctryCurrencyCatCodes": {
      "userCode1": " ",
      "fieldSecurityCode1": " "
    },
    "businessMessaging": {
      "userCode2": " ",
      "fieldSecurityCode2": " "
    },
    "futureUse03": {
      "userCode3": " ",
      "fieldSecurityCode3": " "
    },
    "exceptionProcessing": {
      "userCode4": " ",
      "fieldSecurityCode4": " "
    },
    "accountManagement": {
      "userCode5": " ",
      "fieldSecurityCode5": " "
    },
    "collectionManagement": {
      "userCode6": " ",
      "fieldSecurityCode6": " "
    },
    "authorizations": {
      "userCode7": " ",
      "fieldSecurityCode7": " "
    },
    "customerService": {
      "userCode8": " ",
      "fieldSecurityCode8": " "
    },
    "remoteInterface": {
      "userCode9": " ",
      "fieldSecurityCode9": " "
    },
    "commercialCard": {
      "userCode10": " ",
      "fieldSecurityCode10": " "
    },
    "OfferManagement": {
      "userCode11": " ",
      "fieldSecurityCode11": " "
    },
    "merchantSettlement": {
      "userCode12": " ",
      "fieldSecurityCode12": " "
    },
    "applicationProcessing": {
      "userCode13": " ",
      "fieldSecurityCode13": " "
    },
    "embScriptingSystem": {
      "userCode14": " ",
      "fieldSecurityCode14": " "
    },
    "keyManagementSystem": {
      "userCode15": " ",
      "fieldSecurityCode15": " "
    },
    "futureUse16": {
      "userCode16": " ",
      "fieldSecurityCode16": " "
    },
    "letterRequests": {
      "userCode17": " ",
      "fieldSecurityCode17": " "
    },
    "futureUse18": {
      "userCode18": " ",
      "fieldSecurityCode18": " "
    },
    "internationalLanguage": {
      "userCode19": " ",
      "fieldSecurityCode19": " "
    },
    "rewardManagement": {
      "userCode20": " ",
      "fieldSecurityCode20": " "
    },
    "clientSupport": {
      "userCode21": " ",
      "fieldSecurityCode21": " "
    },
    "security": {
      "userCode22": " ",
      "fieldSecurityCode22": " "
    },
    "connectionManager": {
      "userCode23": " ",
      "fieldSecurityCode23": " "
    },
    "posDeviceManagement": {
      "userCode24": " ",
      "fieldSecurityCode24": " "
    },
    "customerCommunicationManagement": {
      "userCode25": " ",
      "fieldSecurityCode25": " "
    },
    "decisionEngineSystem": {
      "userCode26": " ",
      "fieldSecurityCode26": " "
    },
    "futureUse27": {
      "userCode27": " ",
      "fieldSecurityCode27": " "
    },
    "futureUse28": {
      "userCode28": " ",
      "fieldSecurityCode28": " "
    },
    "transactionManagement": {
      "userCode29": " ",
      "fieldSecurityCode29": " "
    },
    "futureUse30": {
      "userCode30": " ",
      "fieldSecurityCode30": " "
    }
  },
  "businessUnitIncludeExcludeFlag": {
    "businessUnitIncludeExcludeFlag1": {
      "inclusionExclusionFlag1": " ",
      "businessUnit1": " "
    },
    "businessUnitIncludeExcludeFlag2": {
      "inclusionExclusionFlag2": " ",
      "businessUnit2": " "
    },
    "businessUnitIncludeExcludeFlag3": {
      "inclusionExclusionFlag3": " ",
      "businessUnit3": " "
    },
    "businessUnitIncludeExcludeFlag4": {
      "inclusionExclusionFlag4": " ",
      "businessUnit4": " "
    },
    "businessUnitIncludeExcludeFlag5": {
      "inclusionExclusionFlag5": " ",
      "businessUnit5": " "
    },
    "businessUnitIncludeExcludeFlag6": {
      "inclusionExclusionFlag6": " ",
      "businessUnit6": " "
    },
    "businessUnitIncludeExcludeFlag7": {
      "inclusionExclusionFlag7": " ",
      "businessUnit7": " "
    },
    "businessUnitIncludeExcludeFlag8": {
      "inclusionExclusionFlag8": " ",
      "businessUnit8": " "
    },
    "businessUnitIncludeExcludeFlag9": {
      "inclusionExclusionFlag9": " ",
      "businessUnit9": " "
    },
    "businessUnitIncludeExcludeFlag10": {
      "inclusionExclusionFlag10": " ",
      "businessUnit10": " "
    }
  }
}
```

### Error Response Payload

```json
{
  "errorCode": "V5ED0010SF",
  "errorMessage": "Update request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5ED0010SF` | Update request - Record not found |
| `VMSF4001EB` | Client is invalid | 
| `VMSF4002SA` | Client name should not be spaces | 
| `VMSF0112EA` | Org privilege group is invalid | 
| `VMSF0112EB` | Org privilege group does not exist | 
| `VMSF0112EC` | Privilege record is not active | 
| `VMSF0112ED` | Org privilege type does not conform to this user type | 
| `VMSF0108EC` | Oper id in use by another user -please enter another oper id | 
| `VMSF0116EA` | Invalid org include/exclude selection | 
| `VMSF0116EB` | Invalid include/exclude and org selection | 
| `VMSF0302EB` | Invalid selection -use i-include e-exclude or d-delete | 
| `VMSF0303EB` | Valid entry requires entry in incl/excl name and version fields  | 
| `VMSF0303EC` | No service/version selection to include exclude or delete | 
| `VMSF0304EA` | Service/version does not exist- please correct or remove it | 
| `VMSF0304EB` | Service/version is universal & cannot be defined as an override | 
| `VMSF0304EC` | Service/version entered is not allowed | 
| `VMSF0304EE` | Valid entry requires entry in incl/excl name and version fields |