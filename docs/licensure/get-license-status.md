# Get License Status

Retrieves the number of licenses associated with a medical professional
 
```HTTP 
GET {baseUrl}/v1/licensure/{fid}/summary
```

## URI Parameters

| Name | In | Required | Type | Description |
| ---- | -- | -------- | ---- | ----------- |
| `baseUrl` | path | True | string| The API url |
| `fid` | path | True | string | The FID of the practitioner |

## Responses

| Name | Description     | Type  |
| ---- | --------------- | ----- |
| 200  | OK              | [LicenseSummary](../types/licenseSummary.md) |
| 400  | Bad Request     |  |
| 401  | Unauthorized    |  |
| 500  | Server Error    |  |

## Scope

This request requires an OAuth scope of `med.read` in order to execute.

## Example

Input:

```HTTP
GET {baseUrl}/v1/licensure/999999949/summary
```

Output:

```json
{
    "fid": "999999949",
    "count": 1
}
```

For language specific examples go to [samples](/Samples/)
