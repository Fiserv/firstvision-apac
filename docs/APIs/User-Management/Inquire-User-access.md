# Inquire User Access

This service is used to inquire security sign-on data like business unit include/exclude flags and user application access options.

## Endpoint

`GET /v1/users/access`

## Payload Example

### Request Payload

Request Payload

>Should be empty.  
>
***The client id and name should be sent as query parameter.***

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/users/access).

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
  "errorCode": "VMSF0004SF",
  "errorMessage": "Get request - Record not found"  
}
```

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF0004SF` | Get request - Record not found | 
| `VMSF0005SF` | Get Request - Record Add Pending | 
