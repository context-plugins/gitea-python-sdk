
# Action Workflow Runs Response

ActionWorkflowRunsResponse returns ActionWorkflowRuns

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowRunsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `total_count` | `int` | Optional | - |
| `workflow_runs` | [`List[ActionWorkflowRun]`](../../doc/models/action-workflow-run.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_workflow_run import ActionWorkflowRun
from gitea.models.action_workflow_runs_response import ActionWorkflowRunsResponse
from gitea.models.user import User

action_workflow_runs_response = ActionWorkflowRunsResponse(
    total_count=182,
    workflow_runs=[
        ActionWorkflowRun(
            actor=User(
                active=False,
                avatar_url='avatar_url6',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description0',
                email='email6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            conclusion='conclusion8',
            display_title='display_title4',
            event='event4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionWorkflowRun(
            actor=User(
                active=False,
                avatar_url='avatar_url6',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description0',
                email='email6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            conclusion='conclusion8',
            display_title='display_title4',
            event='event4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        ActionWorkflowRun(
            actor=User(
                active=False,
                avatar_url='avatar_url6',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description0',
                email='email6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            conclusion='conclusion8',
            display_title='display_title4',
            event='event4',
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

