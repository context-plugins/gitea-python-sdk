
# Issue Assignees Option

IssueAssigneesOption options for adding/removing issue assignees

*This model accepts additional fields of type Any.*

## Structure

`IssueAssigneesOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignees` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.issue_assignees_option import IssueAssigneesOption

issue_assignees_option = IssueAssigneesOption(
    assignees=[
        'assignees9',
        'assignees0'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

