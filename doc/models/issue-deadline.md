
# Issue Deadline

IssueDeadline represents an issue deadline

*This model accepts additional fields of type Any.*

## Structure

`IssueDeadline`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `due_date` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.issue_deadline import IssueDeadline

issue_deadline = IssueDeadline(
    due_date=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

