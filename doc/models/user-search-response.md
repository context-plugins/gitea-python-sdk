
# User Search Response

*This model accepts additional fields of type Any.*

## Structure

`UserSearchResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[User]`](../../doc/models/user.md) | Optional | - |
| `ok` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.user import User
from giteaapi.models.user_search_response import UserSearchResponse

user_search_response = UserSearchResponse(
    data=[
        User(
            active=False,
            avatar_url='avatar_url6',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description0',
            email='email6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        User(
            active=False,
            avatar_url='avatar_url6',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description0',
            email='email6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        User(
            active=False,
            avatar_url='avatar_url6',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description0',
            email='email6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    ok=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

