
# Issue Labels Option

IssueLabelsOption a collection of labels

*This model accepts additional fields of type Any.*

## Structure

`IssueLabelsOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `List[Any]` | Optional | Labels can be a list of integers representing label IDs<br>or a list of strings representing label names |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.issue_labels_option import IssueLabelsOption

issue_labels_option = IssueLabelsOption(
    labels=[
        jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

