
# New Issue Pins Allowed

NewIssuePinsAllowed represents an API response that says if new Issue Pins are allowed

*This model accepts additional fields of type Any.*

## Structure

`NewIssuePinsAllowed`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `issues` | `bool` | Optional | - |
| `pull_requests` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.new_issue_pins_allowed import NewIssuePinsAllowed

new_issue_pins_allowed = NewIssuePinsAllowed(
    issues=False,
    pull_requests=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

