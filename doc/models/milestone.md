
# Milestone

Milestone milestone is a collection of issues on one repository

*This model accepts additional fields of type Any.*

## Structure

`Milestone`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `closed_at` | `datetime` | Optional | - |
| `closed_issues` | `int` | Optional | ClosedIssues is the number of closed issues in this milestone |
| `created_at` | `datetime` | Optional | - |
| `description` | `str` | Optional | Description provides details about the milestone |
| `due_on` | `datetime` | Optional | - |
| `id` | `int` | Optional | ID is the unique identifier for the milestone |
| `open_issues` | `int` | Optional | OpenIssues is the number of open issues in this milestone |
| `state` | [`State4`](../../doc/models/state-4.md) | Optional | State indicates if the milestone is open or closed<br>open StateOpen pr is opened<br>closed StateClosed pr is closed |
| `title` | `str` | Optional | Title is the title of the milestone |
| `updated_at` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.milestone import Milestone

milestone = Milestone(
    closed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    closed_issues=224,
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    description='description2',
    due_on=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

