
# Action Workflow Job

ActionWorkflowJob represents a WorkflowJob

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowJob`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `datetime` | Optional | - |
| `conclusion` | `str` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `head_branch` | `str` | Optional | - |
| `head_sha` | `str` | Optional | - |
| `html_url` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `labels` | `List[str]` | Optional | - |
| `name` | `str` | Optional | - |
| `run_attempt` | `int` | Optional | - |
| `run_id` | `int` | Optional | - |
| `run_url` | `str` | Optional | - |
| `runner_id` | `int` | Optional | - |
| `runner_name` | `str` | Optional | - |
| `started_at` | `datetime` | Optional | - |
| `status` | `str` | Optional | - |
| `steps` | [`List[ActionWorkflowStep]`](../../doc/models/action-workflow-step.md) | Optional | - |
| `url` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_workflow_job import ActionWorkflowJob

action_workflow_job = ActionWorkflowJob(
    completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    conclusion='conclusion0',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    head_branch='head_branch4',
    head_sha='head_sha2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

