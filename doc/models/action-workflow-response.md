
# Action Workflow Response

ActionWorkflowResponse returns a ActionWorkflow

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total_count` | `int` | Optional | - |
| `workflows` | [`List[ActionWorkflow]`](../../doc/models/action-workflow.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_workflow import ActionWorkflow
from gitea.models.action_workflow_response import ActionWorkflowResponse

action_workflow_response = ActionWorkflowResponse(
    total_count=124,
    workflows=[
        ActionWorkflow(
            badge_url='badge_url8',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            deleted_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            html_url='html_url8',
            id='id2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionWorkflow(
            badge_url='badge_url8',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            deleted_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            html_url='html_url8',
            id='id2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionWorkflow(
            badge_url='badge_url8',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            deleted_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            html_url='html_url8',
            id='id2',
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

