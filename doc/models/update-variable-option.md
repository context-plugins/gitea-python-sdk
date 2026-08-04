
# Update Variable Option

UpdateVariableOption the option when updating variable

*This model accepts additional fields of type Any.*

## Structure

`UpdateVariableOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description of the variable to update |
| `name` | `str` | Optional | New name for the variable. If the field is empty, the variable name won't be updated. |
| `value` | `str` | Required | Value of the variable to update |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.update_variable_option import UpdateVariableOption

update_variable_option = UpdateVariableOption(
    value='value4',
    description='description2',
    name='name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

