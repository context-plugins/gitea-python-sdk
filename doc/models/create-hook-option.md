
# Create Hook Option

CreateHookOption options when create a hook

*This model accepts additional fields of type Any.*

## Structure

`CreateHookOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `bool` | Optional | **Default**: `False` |
| `authorization_header` | `str` | Optional | Authorization header to include in webhook requests |
| `branch_filter` | `str` | Optional | Branch filter pattern to determine which branches trigger the webhook |
| `config` | `Dict[str, str]` | Required | CreateHookOptionConfig has all config options in it<br>required are "content_type" and "url" Required |
| `events` | `List[str]` | Optional | List of events that will trigger this webhook |
| `name` | `str` | Optional | Optional human-readable name for the webhook |
| `mtype` | [`Type`](../../doc/models/type.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_hook_option import CreateHookOption
from gitea.models.mtype import Type

create_hook_option = CreateHookOption(
    config={
        'key0': 'config0',
        'key1': 'config1'
    },
    mtype=Type.MSTEAMS,
    active=False,
    authorization_header='authorization_header4',
    branch_filter='branch_filter8',
    events=[
        'events4',
        'events5'
    ],
    name='name6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

