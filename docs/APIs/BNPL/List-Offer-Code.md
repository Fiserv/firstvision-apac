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
      "businessUnit": 600,
      "productId": 1,
      "offerType": 10,
      "configurationTemplate": "TMPL",
      "bnplType": 0,
      "description": "",
      "configurationTemplateExpiryDate": "12/05/2025"
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
        "instance": "/v1/bnpl/1/listOfferCodes",
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

| ErrorCode |  Description/Values |
| --------  | ------------------ |
| `V5QT0101EA` | No organization record on file |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*
