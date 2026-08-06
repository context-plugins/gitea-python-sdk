
# Edit Team Option

EditTeamOption options for editing a team

*This model accepts additional fields of type Any.*

## Structure

`EditTeamOption`

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
| `visibility` | [`Visibility7`](../../doc/models/visibility-7.md) | Optional | Team visibility within the organization. When omitted, visibility is<br>left unchanged.<br>public TeamVisibilityPublic<br>limited TeamVisibilityLimited<br>private TeamVisibilityPrivate |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_team_option import EditTeamOption
from gitea.models.permission_3 import Permission3

edit_team_option = EditTeamOption(
    name='name4',
    can_create_org_repo=False,
    description='description4',
    includes_all_repositories=False,
    permission=Permission3.READ,
    units=[
        'repo.code',
        'repo.issues',
        'repo.ext_issues',
        'repo.wiki',
        'repo.pulls',
        'repo.releases',
        'repo.projects',
        'repo.ext_wiki'
    ],
    units_map={
        'repo.code': 'read',
        'repo.ext_issues': 'none',
        'repo.ext_wiki': 'none',
        'repo.issues': 'write',
        'repo.projects': 'none',
        'repo.pulls': 'owner',
        'repo.releases': 'none',
        'repo.wiki': 'admin'
    },
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

