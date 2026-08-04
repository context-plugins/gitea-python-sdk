
# Edit Hook Option

EditHookOption options when modify one hook

*This model accepts additional fields of type Any.*

## Structure

`EditHookOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `bool` | Optional | Whether the webhook is active and will be triggered |
| `authorization_header` | `str` | Optional | Authorization header to include in webhook requests |
| `branch_filter` | `str` | Optional | Branch filter pattern to determine which branches trigger the webhook |
| `config` | `Dict[str, str]` | Optional | Configuration settings for the webhook |
| `events` | `List[str]` | Optional | List of events that trigger this webhook |
| `name` | `str` | Optional | Optional human-readable name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.edit_hook_option import EditHookOption

edit_hook_option = EditHookOption(
    active=False,
    authorization_header='authorization_header6',
    branch_filter='branch_filter2',
    config={
        'key0': 'config0',
        'key1': 'config1',
        'key2': 'config2'
    },
    events=[
        'events4'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

