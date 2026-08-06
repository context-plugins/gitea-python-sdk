
# Create Label Option

CreateLabelOption options for creating a label

*This model accepts additional fields of type Any.*

## Structure

`CreateLabelOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `color` | `str` | Required | - |
| `description` | `str` | Optional | Description provides additional context about the label's purpose |
| `exclusive` | `bool` | Optional | - |
| `is_archived` | `bool` | Optional | - |
| `name` | `str` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_label_option import CreateLabelOption

create_label_option = CreateLabelOption(
    color='#00aabb',
    name='name2',
    description='description8',
    exclusive=False,
    is_archived=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

