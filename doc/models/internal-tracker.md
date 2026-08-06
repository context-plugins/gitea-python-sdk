
# Internal Tracker

InternalTracker represents settings for internal tracker

*This model accepts additional fields of type Any.*

## Structure

`InternalTracker`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_only_contributors_to_track_time` | `bool` | Optional | Let only contributors track time (Built-in issue tracker) |
| `enable_issue_dependencies` | `bool` | Optional | Enable dependencies for issues and pull requests (Built-in issue tracker) |
| `enable_time_tracker` | `bool` | Optional | Enable time tracking (Built-in issue tracker) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.internal_tracker import InternalTracker

internal_tracker = InternalTracker(
    allow_only_contributors_to_track_time=False,
    enable_issue_dependencies=False,
    enable_time_tracker=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

