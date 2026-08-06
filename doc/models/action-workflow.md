
# Action Workflow

ActionWorkflow represents a ActionWorkflow

*This model accepts additional fields of type Any.*

## Structure

`ActionWorkflow`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `badge_url` | `str` | Optional | BadgeURL is the URL for the workflow badge |
| `created_at` | `datetime` | Optional | - |
| `deleted_at` | `datetime` | Optional | - |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing the workflow |
| `id` | `str` | Optional | ID is the unique identifier for the workflow |
| `name` | `str` | Optional | Name is the name of the workflow |
| `path` | `str` | Optional | Path is the file path of the workflow |
| `state` | `str` | Optional | State indicates if the workflow is active or disabled |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | URL is the API URL for this workflow |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.action_workflow import ActionWorkflow

action_workflow = ActionWorkflow(
    badge_url='badge_url4',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    deleted_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    html_url='html_url6',
    id='id4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

