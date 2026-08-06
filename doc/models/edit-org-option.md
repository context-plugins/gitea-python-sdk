
# Edit Org Option

EditOrgOption options for editing an organization

*This model accepts additional fields of type Any.*

## Structure

`EditOrgOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | The description of the organization |
| `email` | `str` | Optional | The email address of the organization; use empty string to clear |
| `full_name` | `str` | Optional | The full display name of the organization |
| `location` | `str` | Optional | The location of the organization |
| `repo_admin_change_team_access` | `bool` | Optional | Whether repository administrators can change team access |
| `visibility` | [`Visibility6`](../../doc/models/visibility-6.md) | Optional | possible values are `public`, `limited` or `private`<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `website` | `str` | Optional | The website URL of the organization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_org_option import EditOrgOption

edit_org_option = EditOrgOption(
    description='description8',
    email='email8',
    full_name='full_name4',
    location='location2',
    repo_admin_change_team_access=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

