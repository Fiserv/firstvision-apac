# Check Health

This service is used to verify health of credit management system and authorizaton system. 

## Endpoint

`GET /v1/misc/health`

## Payload Example

### Request Payload


>Should be empty. 
>
>***No input required.***


### Minimum Requirements

The below table contains the mandatory fields required for a successful request. The full request schemas are available in our [API Explorer](../api/?type=get&path=/v1/misc/health).

The below table identifies the required parameters in the request payload.

| Variable | Passed as | Type | Length | Description/Values |
| -------- | :-------: | :--: | :------------: | ------------------ |
>***No mandatory fields required in input.***

### Successful Response Payload

```json
{
  "creditManagementHealthStatus": "0",
  "authorizationHealthStatus": "0"
}
```
