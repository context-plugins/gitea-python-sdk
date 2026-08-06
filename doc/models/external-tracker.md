
# External Tracker

ExternalTracker represents settings for external tracker

*This model accepts additional fields of type Any.*

## Structure

`ExternalTracker`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `external_tracker_format` | `str` | Optional | External Issue Tracker URL Format. Use the placeholders {user}, {repo} and {index} for the username, repository name and issue index. |
| `external_tracker_regexp_pattern` | `str` | Optional | External Issue Tracker issue regular expression |
| `external_tracker_style` | `str` | Optional | External Issue Tracker Number Format, either `numeric`, `alphanumeric`, or `regexp` |
| `external_tracker_url` | `str` | Optional | URL of external issue tracker. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.external_tracker import ExternalTracker

external_tracker = ExternalTracker(
    external_tracker_format='external_tracker_format4',
    external_tracker_regexp_pattern='external_tracker_regexp_pattern2',
    external_tracker_style='external_tracker_style0',
    external_tracker_url='external_tracker_url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

