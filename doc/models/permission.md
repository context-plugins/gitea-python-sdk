
# Permission

Permission represents a set of permissions

*This model accepts additional fields of type Any.*

## Structure

`Permission`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `admin` | `bool` | Optional | - |
| `pull` | `bool` | Optional | - |
| `push` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.permission import Permission

permission = Permission(
    admin=False,
    pull=False,
    push=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

