# Update User Access

This service is used to update security sign-on data like business unit include/exclude flags and user application access options.

## Endpoint

`PUT /v1/users/access`

## Payload Example

### Request Payload

```json
{
  "clientId": 1,
  "name": "NABTEST259",
  "applicationCtryCurrencyCatCodes": {
    "userCode": "1",
    "fieldSecurityCode": "1"
  },
  "applicationBusinessMessaging": {
    "userCode": "2",
    "fieldSecurityCode": "2"
  },
  "applicationFutureUse03": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationExceptionProcessing": {
    "userCode": "3",
    "fieldSecurityCode": "3"
  },
  "applicationAccountManagement": {
    "userCode": "4",
    "fieldSecurityCode": "4"
  },
  "applicationCollectionManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationAuthorizations": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationRemoteInterface": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationCommercialCard": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationOfferManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationMerchantSettlement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationProcessing": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationEmbScriptingSystem": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationKeyManagementSystem": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse16": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationLetterRequests": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationInternationalLanguage": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationRewardManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationClientSupport": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationSecurity": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationConnectionManager": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationPosDeviceManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationCustomerCommunicationManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationpDecisionEngineSystem": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse27": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse28": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationTransactionManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse30": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "businessUnitIncludeExcludeFlag01": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag02": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag03": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag04": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag05": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag06": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag07": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag08": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag09": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "businessUnitIncludeExcludeFlag10": {
    "inclusionExclusionFlag": " ",
    "businessUnit": " "
  },
  "applicationCustomerService": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse18": {
    "userCode": " ",
    "fieldSecurityCode": " "
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
  "applicationAccountManagement": {
    "fieldSecurityCode": "4",
    "userCode": "4"
  },
  "applicationAuthorizations": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationBusinessMessaging": {
    "fieldSecurityCode": "2",
    "userCode": "2"
  },
  "applicationClientSupport": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationCollectionManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationCommercialCard": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationConnectionManager": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationCtryCurrencyCatCodes": {
    "fieldSecurityCode": "1",
    "userCode": "1"
  },
  "applicationCustomerCommunicationManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationCustomerService": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationEmbScriptingSystem": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationExceptionProcessing": {
    "fieldSecurityCode": "3",
    "userCode": "3"
  },
  "applicationFutureUse03": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationFutureUse16": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationFutureUse18": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationFutureUse27": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationFutureUse28": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationFutureUse30": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationInternationalLanguage": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationKeyManagementSystem": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationLetterRequests": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationMerchantSettlement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationOfferManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationPosDeviceManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationProcessing": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationRemoteInterface": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationRewardManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationSecurity": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationTransactionManagement": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "applicationpDecisionEngineSystem": {
    "fieldSecurityCode": " ",
    "userCode": " "
  },
  "businessUnitIncludeExcludeFlag01": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag02": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag03": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag04": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag05": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag06": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag07": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag08": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag09": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "businessUnitIncludeExcludeFlag10": {
    "businessUnit": " ",
    "inclusionExclusionFlag": " "
  },
  "clientId": 1,
  "name": "NABTEST259"
}
```

### Error Response Payload

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/users/access",
    "invalid-params": [
      "VMSF0010SF: Update Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*