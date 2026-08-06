
# Team

Team represents a team in an organization

*This model accepts additional fields of type Any.*

## Structure

`Team`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `can_create_org_repo` | `bool` | Optional | Whether the team can create repositories in the organization |
| `description` | `str` | Optional | The description of the team |
| `id` | `int` | Optional | The unique identifier of the team |
| `includes_all_repositories` | `bool` | Optional | Whether the team has access to all repositories in the organization |
| `name` | `str` | Optional | The name of the team |
| `organization` | [`Organization`](../../doc/models/organization.md) | Optional | Organization represents an organization |
| `permission` | [`Permission1`](../../doc/models/permission-1.md) | Optional | - |
| `units` | `List[str]` | Optional | - |
| `units_map` | `Dict[str, str]` | Optional | - |
| `visibility` | [`Visibility2`](../../doc/models/visibility-2.md) | Optional | Team visibility within the organization. "private" teams are only<br>listable by members and org owners; "limited" teams are listable by<br>any organization member; "public" teams are listable by any signed-in<br>user.<br>public TeamVisibilityPublic<br>limited TeamVisibilityLimited<br>private TeamVisibilityPrivate |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.team import Team

team = Team(
    can_create_org_repo=False,
    description='description0',
    id=128,
    includes_all_repositories=False,
    name='name0',
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

