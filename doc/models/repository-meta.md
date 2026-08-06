
# Repository Meta

RepositoryMeta basic repository information

*This model accepts additional fields of type Any.*

## Structure

`RepositoryMeta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `full_name` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `name` | `str` | Optional | - |
| `owner` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.repository_meta import RepositoryMeta

repository_meta = RepositoryMeta(
    full_name='full_name8',
    id=240,
    name='name2',
    owner='owner6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

