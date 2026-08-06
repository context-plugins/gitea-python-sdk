
# Create Tag Protection Option

CreateTagProtectionOption options for creating a tag protection

*This model accepts additional fields of type Any.*

## Structure

`CreateTagProtectionOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name_pattern` | `str` | Optional | The pattern to match tag names for protection |
| `whitelist_teams` | `List[str]` | Optional | List of team names allowed to create/delete protected tags |
| `whitelist_usernames` | `List[str]` | Optional | List of usernames allowed to create/delete protected tags |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_tag_protection_option import CreateTagProtectionOption

create_tag_protection_option = CreateTagProtectionOption(
    name_pattern='name_pattern4',
    whitelist_teams=[
        'whitelist_teams3',
        'whitelist_teams4'
    ],
    whitelist_usernames=[
        'whitelist_usernames7',
        'whitelist_usernames8',
        'whitelist_usernames9'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

