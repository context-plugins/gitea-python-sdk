
# Update User Avatar Option

UpdateUserAvatarUserOption options when updating the user avatar

*This model accepts additional fields of type Any.*

## Structure

`UpdateUserAvatarOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `str` | Optional | image must be base64 encoded |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.update_user_avatar_option import UpdateUserAvatarOption

update_user_avatar_option = UpdateUserAvatarOption(
    image='image6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

