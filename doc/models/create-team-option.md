
# Create Team Option

CreateTeamOption options for creating a team

*This model accepts additional fields of type Any.*

## Structure

`CreateTeamOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `can_create_org_repo` | `bool` | Optional | Whether the team can create repositories in the organization |
| `description` | `str` | Optional | The description of the team |
| `includes_all_repositories` | `bool` | Optional | Whether the team has access to all repositories in the organization |
| `name` | `str` | Required | - |
| `permission` | [`Permission3`](../../doc/models/permission-3.md) | Optional | - |
| `units` | `List[str]` | Optional | - |
| `units_map` | `Dict[str, str]` | Optional | - |
| `visibility` | [`Visibility4`](../../doc/models/visibility-4.md) | Optional | Team visibility within the organization. Defaults to "private".<br>public TeamVisibilityPublic<br>limited TeamVisibilityLimited<br>private TeamVisibilityPrivate |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_team_option import CreateTeamOption
from giteaapi.models.permission_3 import Permission3

create_team_option = CreateTeamOption(
    name='name2',
    can_create_org_repo=False,
    description='description2',
    includes_all_repositories=False,
    permission=Permission3.WRITE,
    units=[
        'repo.actions',
        'repo.code',
        'repo.issues',
        'repo.ext_issues',
        'repo.wiki',
        'repo.ext_wiki',
        'repo.pulls',
        'repo.releases',
        'repo.projects',
        'repo.ext_wiki'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

