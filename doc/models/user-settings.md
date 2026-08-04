
# User Settings

UserSettings represents user settings

*This model accepts additional fields of type Any.*

## Structure

`UserSettings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | - |
| `diff_view_style` | `str` | Optional | - |
| `full_name` | `str` | Optional | - |
| `hide_activity` | `bool` | Optional | - |
| `hide_email` | `bool` | Optional | Privacy |
| `language` | `str` | Optional | - |
| `location` | `str` | Optional | - |
| `theme` | `str` | Optional | - |
| `website` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.user_settings import UserSettings

user_settings = UserSettings(
    description='description4',
    diff_view_style='diff_view_style8',
    full_name='full_name0',
    hide_activity=False,
    hide_email=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

