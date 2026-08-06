
# Create Action Workflow Dispatch

CreateActionWorkflowDispatch represents the payload for triggering a workflow dispatch event

*This model accepts additional fields of type Any.*

## Structure

`CreateActionWorkflowDispatch`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inputs` | `Dict[str, str]` | Optional | - |
| `ref` | `str` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_action_workflow_dispatch import CreateActionWorkflowDispatch

create_action_workflow_dispatch = CreateActionWorkflowDispatch(
    ref='refs/heads/main',
    inputs={
        'key0': 'inputs6',
        'key1': 'inputs5'
    },
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

