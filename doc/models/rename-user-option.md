
# Rename User Option

RenameUserOption options when renaming a user

*This model accepts additional fields of type Any.*

## Structure

`RenameUserOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `new_username` | `str` | Required | New username for this user. This name cannot be in use yet by any other user. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.rename_user_option import RenameUserOption

rename_user_option = RenameUserOption(
    new_username='new_username2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

