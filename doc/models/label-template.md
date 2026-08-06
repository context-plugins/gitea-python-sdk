
# Label Template

LabelTemplate info of a Label template

*This model accepts additional fields of type Any.*

## Structure

`LabelTemplate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `color` | `str` | Optional | - |
| `description` | `str` | Optional | Description provides additional context about the label template's purpose |
| `exclusive` | `bool` | Optional | - |
| `name` | `str` | Optional | Name is the display name of the label template |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.label_template import LabelTemplate

label_template = LabelTemplate(
    color='00aabb',
    description='description8',
    exclusive=False,
    name='name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

