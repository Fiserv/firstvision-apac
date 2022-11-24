# Inquire User Access

This service is used to inquire security sign-on data like business unit include/exclude flags and user application access options.

## Endpoint

`GET /v1/users/access`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.  
>
***The client id and name should be sent as query parameter.***

<!--
type: tab
-->

```json
{
  "applicationAccountManagement": {
    "fieldSecurityCode": "4",
    "userCode": "4"
  },
  "applicationAuthorizations": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationBusinessMessaging": {
    "fieldSecurityCode": "2",
    "userCode": "2"
  },
  "applicationClientSupport": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationCollectionManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationCommercialCard": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationConnectionManager": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationCtryCurrencyCatCodes": {
    "fieldSecurityCode": "1",
    "userCode": "1"
  },
  "applicationCustomerCommunicationManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationCustomerService": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationEmvScriptingSystem": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationExceptionProcessing": {
    "fieldSecurityCode": "3",
    "userCode": "3"
  },
  "applicationFutureUse03": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationFutureUse16": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationFutureUse18": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationFutureUse27": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationFutureUse28": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationFutureUse30": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationInternationalLanguage": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationKeyManagementSystem": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationLetterRequests": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationMerchantSettlement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationOfferManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationPosDeviceManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationProcessing": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationRemoteInterface": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationRewardManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationSecurity": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationTransactionManagement": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "applicationpDecisionEngineSystem": {
    "fieldSecurityCode": "",
    "userCode": ""
  },
  "businessUnitIncludeExcludeFlag01": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag02": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag03": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag04": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag05": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag06": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag07": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag08": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag09": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "businessUnitIncludeExcludeFlag10": {
    "businessUnit": "",
    "inclusionExclusionFlag": ""
  },
  "clientId": 1,
  "name": "NABTEST259"
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
    "instance": "/v1/users/access",
    "invalid-params": [
      "VMSF0004SF: Get Request - Record not found"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/users/access).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `clientId` | Query Parameter | *number* | 5 | Identification number, referred to as Client ID, assigned to your institution by the processor. | 
| `name` | Query Parameter | *string* | 15 | Sign-on name that the person assigned this User Security Signon record will use to sign on to the system. | 

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `VMSF0004SF` | Get request - Record not found | 
| `VMSF0005SF` | Get Request - Record Add Pending | 

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*