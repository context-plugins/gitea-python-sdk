
# Git Hook

GitHook represents a Git repository hook

*This model accepts additional fields of type Any.*

## Structure

`GitHook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | Content contains the script content of the hook |
| `is_active` | `bool` | Optional | IsActive indicates if the hook is active |
| `name` | `str` | Optional | Name is the name of the Git hook |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.git_hook import GitHook

git_hook = GitHook(
    content='content2',
    is_active=False,
    name='name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

