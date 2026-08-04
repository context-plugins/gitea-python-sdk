
# Edit Tag Protection Option

EditTagProtectionOption options for editing a tag protection

*This model accepts additional fields of type Any.*

## Structure

`EditTagProtectionOption`

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

from giteaapi.models.edit_tag_protection_option import EditTagProtectionOption

edit_tag_protection_option = EditTagProtectionOption(
    name_pattern='name_pattern6',
    whitelist_teams=[
        'whitelist_teams5',
        'whitelist_teams6',
        'whitelist_teams7'
    ],
    whitelist_usernames=[
        'whitelist_usernames9'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

