
# Action Workflow Jobs Response

ActionWorkflowJobsResponse returns ActionWorkflowJobs

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflowJobsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `jobs` | [`List[ActionWorkflowJob]`](../../doc/models/action-workflow-job.md) | Optional | - |
| `total_count` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.action_workflow_job import ActionWorkflowJob
from giteaapi.models.action_workflow_jobs_response import ActionWorkflowJobsResponse

action_workflow_jobs_response = ActionWorkflowJobsResponse(
    jobs=[
        ActionWorkflowJob(
            completed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            conclusion='conclusion8',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            head_branch='head_branch6',
            head_sha='head_sha0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    total_count=230,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

