
# Watch Info

WatchInfo represents an API watch status of one repository

*This model accepts additional fields of type Any.*

## Structure

`WatchInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | The timestamp when the watch status was created |
| `ignored` | `bool` | Optional | Whether notifications for the repository are ignored |
| `reason` | `Any` | Optional | The reason for the current watch status |
| `repository_url` | `str` | Optional | The URL of the repository being watched |
| `subscribed` | `bool` | Optional | Whether the repository is being watched for notifications |
| `url` | `str` | Optional | The URL for managing the watch status |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.watch_info import WatchInfo

watch_info = WatchInfo(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    ignored=False,
    reason=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    repository_url='repository_url0',
    subscribed=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

