
# Action Task Response

ActionTaskResponse returns a ActionTask

*This model accepts additional fields of type Any.*

## Structure

`ActionTaskResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total_count` | `int` | Optional | TotalCount is the total number of workflow runs |
| `workflow_runs` | [`List[ActionTask]`](../../doc/models/action-task.md) | Optional | Entries contains the list of workflow runs |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.action_task import ActionTask
from giteaapi.models.action_task_response import ActionTaskResponse

action_task_response = ActionTaskResponse(
    total_count=14,
    workflow_runs=[
        ActionTask(
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            display_title='display_title4',
            event='event4',
            head_branch='head_branch6',
            head_sha='head_sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionTask(
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            display_title='display_title4',
            event='event4',
            head_branch='head_branch6',
            head_sha='head_sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionTask(
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            display_title='display_title4',
            event='event4',
            head_branch='head_branch6',
            head_sha='head_sha0',
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

