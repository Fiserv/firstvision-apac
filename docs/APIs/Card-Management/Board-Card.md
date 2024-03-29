# Board Card

This API allows to create a new card for an existing account. This API can be invoked with required fields and new card can be generated in real time mode.

Fields that are not provided in the Request object will be initialized to their default values. All numeric fields are initialized to zero and alphanumeric fields initialized to spaces.

## Endpoint

`POST /v1/cards/boardCard`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

```json
{
  "accountId": "0006000012000000263",
  "businessUnit": 600,
  "productId": 1,
  "customerId": "0006000012000000256",
  "cardAction": 1,
  "numberOfCardsRequested": 0,
  "cardType": 0,
  "requestedCardType": 0,
  "cardMailerType": 0,
  "plasticId": " ",
  "name1TypeIndicator": 0,
  "name2TypeIndicator": 0,
  "posServiceCode": 0,
  "cardholderFlag": "0",
  "visaMiniIndicator": "0",
  "programId": 0,
  "mobileDeviceId": "12343",
  "mobileProvisionStatus": "0",
  "deviceIndicator": "0",
  "mccGroupLimits": "100.00",
  "chequeAccountId": " ",
  "savingsAccountId": " ",
  "nameDetails": {
    "embossedName1": "John Brono ",
    "embossedName2": "Samuel Baro",
    "name1": "ABCD",
    "name2": "QWER"
  },
  "addressDetails": {
    "addressLine1": "House no. 12 ",
    "addressLine2": "St. Paul Road ",
    "city": " ",
    "stateprovince": "Uth",
    "postalCode": "1231",
    "addressId": " "
  },
  "physicalVirtualIndicator": "P",
  "isDynamicCVV2Enabled": "0",
  "externalContractId": "0000000000012672379"
}
```

<!--
type: tab
-->

```json
{
  "activationStatus": "0",
  "businessUnit": 600,
  "expiryDate": "18/01/2024",
  "maskedPaymentCardNumber": "0004440010737034347",
  "nameOnCard": "John Brono",
  "paymentInstrumentId": "0004440010737034347",
  "productId": 1
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
    "instance": "/v1/cards/boardCard",
    "invalid-params": [
      "V5S84001EA: ORGANIZATION NOT ON FILE"
    ],
    "source": "VPL",
    "status": 404,
    "title": "Not found"
  }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=post&path=/v1/cards/boardCard).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Leuith | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Payload | *number* | 03 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Payload | *number* | 03 | Unique identification number of the product associated with the organization. Valid values are 1-998. |
| `accountId` | Payload | *string* | 19 | Unique identification number for cardholder billing account.|
| `customerId` | Payload | *string* | 19 | Unique identification number assigned to a customer. |
| `embossedName1` | Payload | *string* | 26 | Name to be embossed on the first embossing line of the card. |
| `cardAction` | Payload | *string* | 1 | This field is the card issue action code that determines the action CMS performs during the next run. |

### Error Codes

Below table provides the list of application's error code and its description.

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5AK4056SA` | Org/Account number combination not found |
| `V5S84003EA` | Base account number is requsted |
| `V5S84003EG` | Base account number must be numeric |
| `V5S84003EH` | Base account number required |
| `V5S84005EA` | Customer na account must be blank |
| `V5S84005EB` | Customer na account required |
| `V5S84005EG` | Customer na account must be blank |
| `V5S84005EH` | Customer na account must be numeric |
| `V5S84008EA` | Relationship not valid for this org |
| `V5S84008EB` | Relationship not valid for the dual org |
| `V5S84001EA` | Organization not on file |
| `V5S84001SA` | Organization not on file |
| `V5S84002EA` | Logo record not on file |
| `V5S84002EB` | Logo record is incomplete |
| `V5S84009EA` | Relationship number required |
| `V5S84011EA` | Insurance not allowed for prepaid accounts |
| `V5S84012EA` | Sweeping not allowed this logo |
| `V5S84012EB` | Hcs must be active for account type values 1,2,3 |
| `V5S84150EI` | No embosser record allowed for control account |
| `V5S84150EJ` | No embosser record allowed for diversion account |
| `V5S84150EK` | No embosser record allowed for billing account |
| `V5AP4061EA` | Number cards required must equal 0 or 1 |
| `V5AP4063EA` | Embossed name type must not equal 3 |
| `V5AP4088EA` | Card delay days value must be numeric |
| `V5AP4097SA` | Card number and account number must be equal for card scheme |
| `V5AP4101SA` | Card number check digit is invalid |
| `V5AP4105SA` | Card sequence already atmaximum for card number |
| `V5AP4106SA` | Card sequence already atmaximum for chip card number |
| `V5AK1512EC` | Invalid DCVV2 method for products supporting both physical and virtual cards |
| `V5AK1512EB` | Invalid DCVV2 method for virtual card |
| `V5AK1512EA` | Invalid DCVV2 method for physical card |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
