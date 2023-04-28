# List Offer Codes

This API is used to fetch the list of offer codes associated for a given business unit and product Id.

## Endpoint

`GET /v1/bnpl/{productId}/listOfferCodes`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty.
>
>***Product id should be sent as path variable and business unit should be sent as query parameter.***

<!--
type: tab
-->

```json
{
    "listOfOfferCodes": [
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPL01TRAN",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPL TRANSACTION VARIANT",
            "configurationTemplateExpiryDate": "03/12/2030"
        },
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPLSNG1",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPL TRAN VARIANT - SINGLE -MONTH 1",
            "configurationTemplateExpiryDate": "30/11/2030"
        },
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPLSNG2",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPL TEMP",
            "configurationTemplateExpiryDate": "01/01/2030"
        },
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPLSNG25",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPLSNG25",
            "configurationTemplateExpiryDate": "01/01/2030"
        },
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPLSNGM2",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPL TRAN VARIANT - SINGLE -MONTH 2",
            "configurationTemplateExpiryDate": "31/12/2030"
        },
        {
            "businessUnit": 700,
            "productId": 0,
            "configurationTemplate": "BNPLSNGM3",
            "offerType": 10,
            "bnplType": 0,
            "description": "BNPL TRAN VARIANT - SINGLE -MONTH 3",
            "configurationTemplateExpiryDate": "31/12/2030"
        }
    ]
}
```

<!--
type: tab
-->

```json
[
    {
        "errorCode": "240009",
        "detail": "Please refer to invalid-params for error details",
        "title": "Required fields missing",
        "instance": "/v1/bnpl/0/listOfferCodes",
        "source": "APT",
        "status": 400,
        "invalid-params": [
            "businessUnit: This field should not be empty"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/bnpl/{productId}/listOfferCodes).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `businessUnit` | Query Parameter | *number* | 3 | Unique identification number associated with the organization. Valid values from 1-998. |
| `productId` | Path Variable | *number* | 3 | Unique identification number of the product associated with the organization. If the table is defined at organization level, populate this field as zeroes. For tables defined at product level, valid values are 1-998. |

### Error Codes

Below table provides the list of application's error code and its description.

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
