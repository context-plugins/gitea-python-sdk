
# Add Collaborator Option

AddCollaboratorOption options when adding a user as a collaborator of a repository

*This model accepts additional fields of type Any.*

## Structure

`AddCollaboratorOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `permission` | [`Permission2`](../../doc/models/permission-2.md) | Optional | Permission level to grant the collaborator<br>read RepoWritePermissionRead<br>write RepoWritePermissionWrite<br>admin RepoWritePermissionAdmin |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.add_collaborator_option import AddCollaboratorOption
from gitea.models.permission_2 import Permission2

add_collaborator_option = AddCollaboratorOption(
    permission=Permission2.READ,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

