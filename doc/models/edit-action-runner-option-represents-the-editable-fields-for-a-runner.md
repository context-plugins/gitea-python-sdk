
# Edit Action Runner Option Represents the Editable Fields for a Runner

*This model accepts additional fields of type Any.*

## Structure

`EditActionRunnerOptionRepresentsTheEditableFieldsForARunner`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `disabled` | `bool` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.edit_action_runner_option_represents_the_editable_fields_for_a_runner import EditActionRunnerOptionRepresentsTheEditableFieldsForARunner

edit_action_runner_option_represents_the_editable_fields_for_a_runner = EditActionRunnerOptionRepresentsTheEditableFieldsForARunner(
    disabled=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

