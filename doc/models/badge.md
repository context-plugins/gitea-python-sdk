
# Badge

Badge represents a user badge

*This model accepts additional fields of type Any.*

## Structure

`Badge`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `image_url` | `str` | Optional | - |
| `slug` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.badge import Badge

badge = Badge(
    description='description0',
    id=184,
    image_url='image_url6',
    slug='slug6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

