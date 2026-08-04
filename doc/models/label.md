
# Label

Label a label to an issue or a pr

*This model accepts additional fields of type Any.*

## Structure

`Label`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `color` | `str` | Optional | - |
| `description` | `str` | Optional | Description provides additional context about the label's purpose |
| `exclusive` | `bool` | Optional | - |
| `id` | `int` | Optional | ID is the unique identifier for the label |
| `is_archived` | `bool` | Optional | - |
| `name` | `str` | Optional | Name is the display name of the label |
| `url` | `str` | Optional | URL is the API endpoint for accessing this label |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.label import Label

label = Label(
    color='00aabb',
    description='description0',
    exclusive=False,
    id=22,
    is_archived=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

