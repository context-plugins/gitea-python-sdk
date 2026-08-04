
# Action Task

ActionTask represents a ActionTask

*This model accepts additional fields of type Any.*

## Structure

`ActionTask`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `display_title` | `str` | Optional | DisplayTitle is the display title for the workflow run |
| `event` | `str` | Optional | Event is the type of event that triggered the workflow |
| `head_branch` | `str` | Optional | HeadBranch is the branch that triggered the workflow |
| `head_sha` | `str` | Optional | HeadSHA is the commit SHA that triggered the workflow |
| `id` | `int` | Optional | ID is the unique identifier for the action task |
| `name` | `str` | Optional | Name is the name of the workflow |
| `run_number` | `int` | Optional | RunNumber is the sequential number of the workflow run |
| `run_started_at` | `datetime` | Optional | - |
| `status` | `str` | Optional | Status indicates the current status of the workflow run |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | URL is the API URL for this workflow run |
| `workflow_id` | `str` | Optional | WorkflowID is the identifier of the workflow |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.action_task import ActionTask

action_task = ActionTask(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    display_title='display_title4',
    event='event4',
    head_branch='head_branch4',
    head_sha='head_sha0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

