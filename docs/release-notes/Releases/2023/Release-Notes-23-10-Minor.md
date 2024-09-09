# Release 23.10-Minor - Version 1.5.0

## Date: 23/10/2023

### General Changes

- Get Access Token: Restrict the access token for a given region for all APIs.

#### Documentation Change in Swagger

N/A

### New APIs

#### Generate Dynamic CVV2(version 2)

This API is used to generate encrypted dynamic CVV2 and provide other additional details like encrypted payment card number, encrypted expiry date, embossed name 1, embossed name 2, dynamic CVV2 expire date and time for a given payment instrument Id.This is new version 2 build for Generate Dynamic CVV2 API changes are done similar to other POST API's where query/path variables are removed.

### Updated APIs

| S.No |  Category            | API Name                  | Change                                                                                     |
|------|----------------------|---------------------------|--------------------------------------------------------------------------------------------|
| 1    | Account Management   | Update Account Charge-Off | • Added below field in request  • chargeOffStatus  • Changed below fields type from mandatory to optional in input request   • chargeOffReason  • notificationReceivedDate                                                               |
| 2    | Authorization        | Request Authorization     | • Removed default values passed for address/zipcode in request. These are hidden fields,hence no change in request message                                                       |

### Deleted APIs

N/A
