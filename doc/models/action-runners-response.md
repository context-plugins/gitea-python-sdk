
# Action Runners Response

ActionRunnersResponse returns Runners

*This model accepts additional fields of type Any.*

## Structure

`ActionRunnersResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `runners` | [`List[ActionRunner]`](../../doc/models/action-runner.md) | Optional | - |
| `total_count` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.action_runner import ActionRunner
from giteaapi.models.action_runner_label import ActionRunnerLabel
from giteaapi.models.action_runners_response import ActionRunnersResponse

action_runners_response = ActionRunnersResponse(
    runners=[
        ActionRunner(
            busy=False,
            disabled=False,
            ephemeral=False,
            id=78,
            labels=[
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
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
        ),
        ActionRunner(
            busy=False,
            disabled=False,
            ephemeral=False,
            id=78,
            labels=[
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
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
        ),
        ActionRunner(
            busy=False,
            disabled=False,
            ephemeral=False,
            id=78,
            labels=[
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                ActionRunnerLabel(
                    id=236,
                    name='name8',
                    mtype='type2',
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
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
    ],
    total_count=202,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

