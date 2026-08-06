
# Action Runner Label

ActionRunnerLabel represents a Runner Label

*This model accepts additional fields of type Any.*

## Structure

`ActionRunnerLabel`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | - |
| `name` | `str` | Optional | - |
| `mtype` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.action_runner_label import ActionRunnerLabel

action_runner_label = ActionRunnerLabel(
    id=172,
    name='name0',
    mtype='type0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

