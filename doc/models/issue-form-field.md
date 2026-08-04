
# Issue Form Field

IssueFormField represents a form field

*This model accepts additional fields of type Any.*

## Structure

`IssueFormField`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attributes` | `Dict[str, Any]` | Optional | - |
| `id` | `str` | Optional | - |
| `mtype` | [`Type1`](../../doc/models/type-1.md) | Optional | - |
| `validations` | `Dict[str, Any]` | Optional | - |
| `visible` | [`List[Visible]`](../../doc/models/visible.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.issue_form_field import IssueFormField
from giteaapi.models.type_1 import Type1
from giteaapi.models.visible import Visible

issue_form_field = IssueFormField(
    attributes={
        'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        'key1': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
        'key2': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    },
    id='id8',
    mtype=Type1.INPUT,
    validations={
        'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    },
    visible=[
        Visible.FORM,
        Visible.CONTENT
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

