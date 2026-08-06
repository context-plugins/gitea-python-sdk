
# Action Runner

ActionRunner represents a Runner

*This model accepts additional fields of type Any.*

## Structure

`ActionRunner`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `busy` | `bool` | Optional | - |
| `disabled` | `bool` | Optional | - |
| `ephemeral` | `bool` | Optional | - |
| `id` | `int` | Optional | - |
| `labels` | [`List[ActionRunnerLabel]`](../../doc/models/action-runner-label.md) | Optional | - |
| `name` | `str` | Optional | - |
| `status` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.action_runner import ActionRunner
from gitea.models.action_runner_label import ActionRunnerLabel

action_runner = ActionRunner(
    busy=False,
    disabled=False,
    ephemeral=False,
    id=234,
    labels=[
        ActionRunnerLabel(
            id=236,
            name='name8',
            mtype='type2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

