
# Organization

Organization represents an organization

*This model accepts additional fields of type Any.*

## Structure

`Organization`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `avatar_url` | `str` | Optional | The URL of the organization's avatar |
| `description` | `str` | Optional | The description of the organization |
| `email` | `str` | Optional | The email address of the organization |
| `full_name` | `str` | Optional | The full display name of the organization |
| `id` | `int` | Optional | The unique identifier of the organization |
| `location` | `str` | Optional | The location of the organization |
| `name` | `str` | Optional | The name of the organization |
| `repo_admin_change_team_access` | `bool` | Optional | Whether repository administrators can change team access |
| `username` | `str` | Optional | username of the organization<br>deprecated |
| `visibility` | [`Visibility1`](../../doc/models/visibility-1.md) | Optional | The visibility level of the organization (public, limited, private)<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `website` | `str` | Optional | The website URL of the organization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.organization import Organization

organization = Organization(
    avatar_url='avatar_url2',
    description='description6',
    email='email0',
    full_name='full_name2',
    id=8,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

