
# Edit Git Hook Option

EditGitHookOption options when modifying one Git hook

*This model accepts additional fields of type Any.*

## Structure

`EditGitHookOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | Content is the new script content for the hook |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.edit_git_hook_option import EditGitHookOption

edit_git_hook_option = EditGitHookOption(
    content='content6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

