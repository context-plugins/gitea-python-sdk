
# Create Fork Option

CreateForkOption options for creating a fork

*This model accepts additional fields of type Any.*

## Structure

`CreateForkOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | name of the forked repository |
| `organization` | `str` | Optional | organization name, if forking into an organization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_fork_option import CreateForkOption

create_fork_option = CreateForkOption(
    name='name0',
    organization='organization4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

