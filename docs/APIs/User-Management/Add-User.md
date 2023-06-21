# Add User

This API is used to add new security sign-on entity. This newly created entity determine the person’s access rights on the system. Sign-on entity must be setup and active for each person authorized to access the system.

*More than one person cannot sign on to the system using the same sign-on entity. A single person cannot sign on using the same sign-on entity at multiple terminals at the same time.*

## Endpoint

`POST /v1/users/boardUser`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

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
  "applicationCtryCurrencyCatCodes": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationFutureUse03": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationExceptionProcessing": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationAccountManagement": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationAuthorizations": {
    "userCode": " ",
    "fieldSecurityCode": " "
  },
  "applicationCustomerService": {
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
    "userCode29": " ",
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
  "userServicePrivilege01": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege02": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege03": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege04": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege05": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege06": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege07": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege08": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege09": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  },
  "userServicePrivilege10": {
    "serviceInclusionExclusionflag": " ",
    "serviceName": " ",
    "serviceVersion": " "
  }
}
```

<!--
type: tab
-->

```json
{}

```

<!--
type: tab
-->

```json
[
  {
    "detail": "Please refer to invalid-params for error details",
    "errorCode": "440401",
    "instance": "/v1/users/boardUser",
    "invalid-params": [
      "VMSF0028SF: Record ADDED, SAVE not allowed."
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

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

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF0028SF`  |  Record added, save not allowed |
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

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
