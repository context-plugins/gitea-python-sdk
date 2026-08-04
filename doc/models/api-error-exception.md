
# Api Error Exception

APIError is an api error with a message

*This model accepts additional fields of type Any.*

## Structure

`ApiErrorException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | Message contains the error description |
| `url` | `str` | Optional | URL contains the documentation URL for this error |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
try:
    # make the API call
except ApiErrorException as e:
    print(e)
except ApiException as e:
    print(e)
```

