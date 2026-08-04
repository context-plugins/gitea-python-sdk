
# Lock Issue Option

LockIssueOption options to lock an issue

*This model accepts additional fields of type Any.*

## Structure

`LockIssueOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lock_reason` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.lock_issue_option import LockIssueOption

lock_issue_option = LockIssueOption(
    lock_reason='lock_reason6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

