
# Action Workflow Step

ActionWorkflowStep represents a step of a WorkflowJob

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowStep`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `datetime` | Optional | - |
| `conclusion` | `str` | Optional | - |
| `name` | `str` | Optional | - |
| `number` | `int` | Optional | - |
| `started_at` | `datetime` | Optional | - |
| `status` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_workflow_step import ActionWorkflowStep

action_workflow_step = ActionWorkflowStep(
    completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    conclusion='conclusion2',
    name='name8',
    number=70,
    started_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

