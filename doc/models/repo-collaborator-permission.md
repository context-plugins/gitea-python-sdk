
# Repo Collaborator Permission

RepoCollaboratorPermission to get repository permission for a collaborator

*This model accepts additional fields of type Any.*

## Structure

`RepoCollaboratorPermission`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `permission` | [`Permission5`](../../doc/models/permission-5.md) | Optional | Permission level of the collaborator<br>none AccessLevelNameNone<br>read AccessLevelNameRead<br>write AccessLevelNameWrite<br>admin AccessLevelNameAdmin<br>owner AccessLevelNameOwner |
| `role_name` | `str` | Optional | RoleName is the name of the permission role |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.permission_5 import Permission5
from giteaapi.models.repo_collaborator_permission import RepoCollaboratorPermission
from giteaapi.models.user import User

repo_collaborator_permission = RepoCollaboratorPermission(
    permission=Permission5.OWNER,
    role_name='role_name2',
    user=User(
        active=False,
        avatar_url='avatar_url6',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description0',
        email='email6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

