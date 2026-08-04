
# Tag Protection

TagProtection represents a tag protection

*This model accepts additional fields of type Any.*

## Structure

`TagProtection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `id` | `int` | Optional | The unique identifier of the tag protection |
| `name_pattern` | `str` | Optional | The pattern to match tag names for protection |
| `updated_at` | `datetime` | Optional | - |
| `whitelist_teams` | `List[str]` | Optional | List of team names allowed to create/delete protected tags |
| `whitelist_usernames` | `List[str]` | Optional | List of usernames allowed to create/delete protected tags |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.tag_protection import TagProtection

tag_protection = TagProtection(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=36,
    name_pattern='name_pattern8',
    updated_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    whitelist_teams=[
        'whitelist_teams7'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

