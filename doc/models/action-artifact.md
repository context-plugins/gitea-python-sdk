
# Action Artifact

ActionArtifact represents a ActionArtifact

*This model accepts additional fields of type Any.*

## Structure

`ActionArtifact`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `archive_download_url` | `str` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `expired` | `bool` | Optional | - |
| `expires_at` | `datetime` | Optional | - |
| `id` | `int` | Optional | - |
| `name` | `str` | Optional | - |
| `size_in_bytes` | `int` | Optional | - |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | - |
| `workflow_run` | [`ActionWorkflowRun`](../../doc/models/action-workflow-run.md) | Optional | ActionWorkflowRun represents a WorkflowRun |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_artifact import ActionArtifact

action_artifact = ActionArtifact(
    archive_download_url='archive_download_url6',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    expired=False,
    expires_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    id=154,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

