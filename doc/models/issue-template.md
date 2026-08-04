
# Issue Template

IssueTemplate represents an issue template for a repository

*This model accepts additional fields of type Any.*

## Structure

`IssueTemplate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `about` | `str` | Optional | - |
| `assignees` | `List[str]` | Optional | - |
| `body` | [`List[IssueFormField]`](../../doc/models/issue-form-field.md) | Optional | - |
| `content` | `str` | Optional | - |
| `file_name` | `str` | Optional | - |
| `labels` | `List[str]` | Optional | - |
| `name` | `str` | Optional | - |
| `ref` | `str` | Optional | - |
| `title` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.issue_form_field import IssueFormField
from giteaapi.models.issue_template import IssueTemplate
from giteaapi.models.type_1 import Type1
from giteaapi.models.visible import Visible

issue_template = IssueTemplate(
    about='about0',
    assignees=[
        'assignees5',
        'assignees6'
    ],
    body=[
        IssueFormField(
            attributes={
                'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key1': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            },
            id='id6',
            mtype=Type1.CHECKBOXES,
            validations={
                'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key1': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key2': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            },
            visible=[
                Visible.FORM,
                Visible.CONTENT,
                Visible.FORM
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        IssueFormField(
            attributes={
                'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key1': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            },
            id='id6',
            mtype=Type1.CHECKBOXES,
            validations={
                'key0': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key1': jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
                'key2': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            },
            visible=[
                Visible.FORM,
                Visible.CONTENT,
                Visible.FORM
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    content='content8',
    file_name='file_name4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

