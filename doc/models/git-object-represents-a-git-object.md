
# Git Object Represents a Git Object

*This model accepts additional fields of type Any.*

## Structure

`GitObjectRepresentsAGitObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sha` | `str` | Optional | The SHA hash of the Git object |
| `mtype` | `str` | Optional | The type of the Git object (e.g., commit, tag, tree, blob) |
| `url` | `str` | Optional | The URL to access this Git object |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.git_object_represents_a_git_object import GitObjectRepresentsAGitObject

git_object_represents_a_git_object = GitObjectRepresentsAGitObject(
    sha='sha4',
    mtype='type2',
    url='url2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

