
# Reference Represents a Git Reference

*This model accepts additional fields of type Any.*

## Structure

`ReferenceRepresentsAGitReference`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `object` | [`GitObjectRepresentsAGitObject`](../../doc/models/git-object-represents-a-git-object.md) | Optional | - |
| `ref` | `str` | Optional | The name of the Git reference (e.g., refs/heads/main) |
| `url` | `str` | Optional | The URL to access this Git reference |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.git_object_represents_a_git_object import GitObjectRepresentsAGitObject
from gitea.models.reference_represents_a_git_reference import ReferenceRepresentsAGitReference

reference_represents_a_git_reference = ReferenceRepresentsAGitReference(
    object=GitObjectRepresentsAGitObject(
        sha='sha8',
        mtype='type8',
        url='url6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    ref='ref4',
    url='url8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

