
# Identity

Identity for a person's identity like an author or committer

*This model accepts additional fields of type Any.*

## Structure

`Identity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `name` | `str` | Optional | Name is the person's name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.identity import Identity

identity = Identity(
    email='email2',
    name='name4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

