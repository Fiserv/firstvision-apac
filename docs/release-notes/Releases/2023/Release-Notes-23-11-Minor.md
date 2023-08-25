# Release 23.11-Minor - Version 1.6.0

## Date: 23/11/2023

### General Changes

- NA

#### Documentation Change in Swagger

- Post Payments: Removed actionCode, representativeDetails group and fields under this group from request
- Board Entities: New value 'B' added under physicalvirtualIndicator in request
- Board Entities V2: New value 'B' added under physicalvirtualIndicator in request
- Board Cards: New value 'B' added under physicalvirtualIndicator in request
- Inquire Card : New value 'B' added under physicalvirtualIndicator in request
- Inquire Product: New field physicalvirtualIndicator added in response

### New APIs

#### Directed Post Payments

This API is used to add payments on a specific plan Id and account Id given. This API updates the open-to-buy, memo credit in real time on customer's account and and generate an outstanding authorization record.

#### Inquire MCC Limits

This API is used to fetch the MCC limits to control the card usage. These MCC limits are updated at individual card level.

#### Update MCC Limits

This API is used to update the MCC limits to control the card usage. These MCC limits are updated at individual card level.

### Updated APIs

| S.No |  Category | API Name |  Change |
| :---  | :------- |  :------ | :------- |
| 1 | Account Management | Post Payments | <ul> <li>  Removed actionCode from request and defaulted the value in it <li> Removed 'representativeDetails’ group and fields under this group
| 2 | Card Management | Board Card | <ul> <li>  Added new valid value 'B' under existing field physicalvirtualIndicator in request
| 3 | Card Management | Inquire Card | <ul> <li>  Added new valid value 'B' under existing field physicalvirtualIndicator in request
| 4 | Product Management | Inquire Product | <ul> <li>  Added new field physicalvirtualIndicator in response
| 5 | Miscellaneous | Board Entities | <ul> <li>  Added new valid value 'B' under existing field physicalvirtualIndicator in request
| 6 | Miscellaneous | Board Entities V2 | <ul> <li>  Added new valid value 'B' under existing field physicalvirtualIndicator in request

### Deleted APIs

N/A
