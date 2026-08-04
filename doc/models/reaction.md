
# Reaction

Reaction contain one reaction

*This model accepts additional fields of type Any.*

## Structure

`Reaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | The reaction content (e.g., emoji or reaction type) |
| `created_at` | `datetime` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.reaction import Reaction
from giteaapi.models.user import User

reaction = Reaction(
    content='content6',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    user=User(
        active=False,
        avatar_url='avatar_url6',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description0',
        email='email6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

