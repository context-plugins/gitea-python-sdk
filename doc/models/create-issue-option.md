
# Create Issue Option

CreateIssueOption options to create one issue

*This model accepts additional fields of type Any.*

## Structure

`CreateIssueOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee` | `str` | Optional | deprecated |
| `assignees` | `List[str]` | Optional | - |
| `body` | `str` | Optional | - |
| `closed` | `bool` | Optional | - |
| `due_date` | `datetime` | Optional | - |
| `labels` | `List[int]` | Optional | list of label ids |
| `milestone` | `int` | Optional | milestone id |
| `projects` | `List[int]` | Optional | list of project ids |
| `ref` | `str` | Optional | - |
| `title` | `str` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.create_issue_option import CreateIssueOption

create_issue_option = CreateIssueOption(
    title='title6',
    assignee='assignee0',
    assignees=[
        'assignees9'
    ],
    body='body4',
    closed=False,
    due_date=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

