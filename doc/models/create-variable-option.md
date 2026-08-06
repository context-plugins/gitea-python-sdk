
# Create Variable Option

CreateVariableOption the option when creating variable

*This model accepts additional fields of type Any.*

## Structure

`CreateVariableOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description of the variable to create |
| `value` | `str` | Required | Value of the variable to create |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_variable_option import CreateVariableOption

create_variable_option = CreateVariableOption(
    value='value0',
    description='description2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

