
# Push Mirror

PushMirror represents information of a push mirror

*This model accepts additional fields of type Any.*

## Structure

`PushMirror`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | - |
| `interval` | `str` | Optional | The sync interval for automatic updates |
| `last_error` | `str` | Optional | The last error message encountered during sync |
| `last_update` | `datetime` | Optional | - |
| `remote_address` | `str` | Optional | The remote repository URL being mirrored to |
| `remote_name` | `str` | Optional | The name of the remote in the git configuration |
| `repo_name` | `str` | Optional | The name of the source repository |
| `sync_on_commit` | `bool` | Optional | Whether to sync on every commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.push_mirror import PushMirror

push_mirror = PushMirror(
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    interval='interval4',
    last_error='last_error8',
    last_update=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    remote_address='remote_address0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

