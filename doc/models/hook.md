
# Hook

Hook a hook is a web hook when one repository changed

*This model accepts additional fields of type Any.*

## Structure

`Hook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `bool` | Optional | Whether the webhook is active and will be triggered |
| `authorization_header` | `str` | Optional | Authorization header to include in webhook requests |
| `branch_filter` | `str` | Optional | Branch filter pattern to determine which branches trigger the webhook |
| `config` | `Dict[str, str]` | Optional | Configuration settings for the webhook |
| `created_at` | `datetime` | Optional | - |
| `events` | `List[str]` | Optional | List of events that trigger this webhook |
| `id` | `int` | Optional | The unique identifier of the webhook |
| `name` | `str` | Optional | Optional human-readable name for the webhook |
| `mtype` | `str` | Optional | The type of the webhook (e.g., gitea, slack, discord) |
| `updated_at` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.hook import Hook

hook = Hook(
    active=False,
    authorization_header='authorization_header6',
    branch_filter='branch_filter8',
    config={
        'key0': 'config0',
        'key1': 'config1'
    },
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

