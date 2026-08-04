
# Action Variable

ActionVariable return value of the query API

*This model accepts additional fields of type Any.*

## Structure

`ActionVariable`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | `str` | Optional | the value of the variable |
| `description` | `str` | Optional | the description of the variable |
| `name` | `str` | Optional | the name of the variable |
| `owner_id` | `int` | Optional | the owner to which the variable belongs |
| `repo_id` | `int` | Optional | the repository to which the variable belongs |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.action_variable import ActionVariable

action_variable = ActionVariable(
    data='data2',
    description='description2',
    name='name2',
    owner_id=200,
    repo_id=192,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

