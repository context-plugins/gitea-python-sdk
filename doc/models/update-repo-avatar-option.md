
# Update Repo Avatar Option

UpdateRepoAvatarUserOption options when updating the repo avatar

*This model accepts additional fields of type Any.*

## Structure

`UpdateRepoAvatarOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `str` | Optional | image must be base64 encoded |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.update_repo_avatar_option import UpdateRepoAvatarOption

update_repo_avatar_option = UpdateRepoAvatarOption(
    image='image6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

