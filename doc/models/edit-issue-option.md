
# Edit Issue Option

EditIssueOption options for editing an issue

*This model accepts additional fields of type Any.*

## Structure

`EditIssueOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee` | `str` | Optional | deprecated |
| `assignees` | `List[str]` | Optional | - |
| `body` | `str` | Optional | - |
| `content_version` | `int` | Optional | The current version of the issue content to detect conflicts during editing |
| `due_date` | `datetime` | Optional | - |
| `milestone` | `int` | Optional | - |
| `projects` | `List[int]` | Optional | list of project ids to set (replaces existing projects) |
| `ref` | `str` | Optional | - |
| `state` | `str` | Optional | - |
| `title` | `str` | Optional | - |
| `unset_due_date` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.edit_issue_option import EditIssueOption

edit_issue_option = EditIssueOption(
    assignee='assignee6',
    assignees=[
        'assignees5',
        'assignees6',
        'assignees7'
    ],
    body='body0',
    content_version=206,
    due_date=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

