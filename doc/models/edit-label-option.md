
# Edit Label Option

EditLabelOption options for editing a label

*This model accepts additional fields of type Any.*

## Structure

`EditLabelOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `color` | `str` | Optional | - |
| `description` | `str` | Optional | Description provides additional context about the label's purpose |
| `exclusive` | `bool` | Optional | - |
| `is_archived` | `bool` | Optional | - |
| `name` | `str` | Optional | Name is the new display name for the label |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_label_option import EditLabelOption

edit_label_option = EditLabelOption(
    color='#00aabb',
    description='description4',
    exclusive=False,
    is_archived=False,
    name='name4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

