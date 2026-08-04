
# Create Access Token Option

CreateAccessTokenOption options when create access token

*This model accepts additional fields of type Any.*

## Structure

`CreateAccessTokenOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | - |
| `scopes` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_access_token_option import CreateAccessTokenOption

create_access_token_option = CreateAccessTokenOption(
    name='name6',
    scopes=[
        'all',
        'read:activitypub',
        'read:issue',
        'write:misc',
        'read:notification',
        'read:organization',
        'read:package',
        'read:repository',
        'read:user'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

