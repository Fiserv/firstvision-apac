# Fetch Customer ID from Clear PAN

This service is used to fetch customer identification for the requested First Vision's clear PAN given in encrypted format.

## Endpoint

`GET /v1/cards/{encryptedPaymentCardNumber}/customerId`

## Payload Example

<!--
type: tab
titles: Request, Response, Error
-->

>Should be empty. 
>
>***The Encrypted Payment Card Number should be sent as path variable.***

<!--
type: tab
--> 

```json
{
  "customerId": "0006000011000000707"
}
```

<!--
type: tab
--> 

```json
[
    {
        "errorCode": "440401",
        "detail": "Please refer to invalid-params for error details",
        "title": "Not found",
        "instance": "/v1/cards/217E8A00536C7A101B055563FBF49C9A/customerId",
        "source": "VPL",
        "status": 404,
        "invalid-params": [
            "V5CG4002EF: Provide valid 32byte encrypted card number"
        ]
    }
]
```

<!-- type: tab-end -->

### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/cards/{encryptedPaymentCardNumber}/customerId).

The below table identifies the required query parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
| `encryptedPaymentCardNumber` | Path Variable | *string* | 32 | Unique identification number that appears on the front of the card (PAN) in encrypted format. |

### Error Codes 

Below table provides the list of application's error code and its description.

| ErrorCode |  Description |
| --------  | ------------------ |
|`V5CG4002EA` | Card number must be provided |                                
|`V5CG4002EF` | Provide valid 32byte encrypted card number |                      
|`V5CG4002EG` | Invalid card number or organization not deteremined |            
|`V5CG4002EH` | Card nbr decryption failed |                                      
|`V5CG4002EC` | Card number not found |                                           
|`V5CG4002ED` | Card number already purged |                                      
|`V5CG4002EE` | Card number is in add pending |                                   
|`V5CG4002EI` | Org should be entered |                                           
|`V5CG4002EJ` | Org is not found or add pending |

*In addition to the above mentioned error codes, please refer this link for common error codes [Common Error Codes](?path=docs/Common_Error_Code.md).*