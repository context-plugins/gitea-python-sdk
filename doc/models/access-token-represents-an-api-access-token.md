
# Access Token Represents an Api Access Token

*This model accepts additional fields of type Any.*

## Structure

`AccessTokenRepresentsAnApiAccessToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | The timestamp when the token was created |
| `id` | `int` | Optional | The unique identifier of the access token |
| `last_used_at` | `datetime` | Optional | The timestamp when the token was last used |
| `name` | `str` | Optional | The name of the access token |
| `scopes` | `List[str]` | Optional | The scopes granted to this access token |
| `sha_1` | `str` | Optional | The SHA1 hash of the access token |
| `token_last_eight` | `str` | Optional | The last eight characters of the token |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.access_token_represents_an_api_access_token import AccessTokenRepresentsAnApiAccessToken

access_token_represents_an_api_access_token = AccessTokenRepresentsAnApiAccessToken(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=204,
    last_used_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    name='name4',
    scopes=[
        'scopes8',
        'scopes9'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

