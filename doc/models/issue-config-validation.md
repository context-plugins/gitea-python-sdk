
# Issue Config Validation

*This model accepts additional fields of type Any.*

## Structure

`IssueConfigValidation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | - |
| `valid` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.issue_config_validation import IssueConfigValidation

issue_config_validation = IssueConfigValidation(
    message='message6',
    valid=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

