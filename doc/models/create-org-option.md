
# Create Org Option

CreateOrgOption options for creating an organization

*This model accepts additional fields of type Any.*

## Structure

`CreateOrgOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | The description of the organization |
| `email` | `str` | Optional | The email address of the organization |
| `full_name` | `str` | Optional | The full display name of the organization |
| `location` | `str` | Optional | The location of the organization |
| `repo_admin_change_team_access` | `bool` | Optional | Whether repository administrators can change team access |
| `username` | `str` | Required | username of the organization |
| `visibility` | [`Visibility3`](../../doc/models/visibility-3.md) | Optional | possible values are `public` (default), `limited` or `private`<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `website` | `str` | Optional | The website URL of the organization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_org_option import CreateOrgOption

create_org_option = CreateOrgOption(
    username='username0',
    description='description0',
    email='email6',
    full_name='full_name6',
    location='location4',
    repo_admin_change_team_access=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

