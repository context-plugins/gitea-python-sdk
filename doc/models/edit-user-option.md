
# Edit User Option

EditUserOption edit user options

*This model accepts additional fields of type Any.*

## Structure

`EditUserOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `bool` | Optional | Whether the user account is active |
| `admin` | `bool` | Optional | Whether the user has administrator privileges |
| `allow_create_organization` | `bool` | Optional | Whether the user can create organizations |
| `allow_git_hook` | `bool` | Optional | Whether the user can use Git hooks |
| `allow_import_local` | `bool` | Optional | Whether the user can import local repositories |
| `description` | `str` | Optional | The user's personal description or bio |
| `email` | `str` | Optional | - |
| `full_name` | `str` | Optional | The full display name of the user |
| `location` | `str` | Optional | The user's location or address |
| `login_name` | `str` | Required | identifier of the user, provided by the external authenticator (if configured)<br><br>**Default**: `"empty"` |
| `max_repo_creation` | `int` | Optional | Maximum number of repositories the user can create |
| `must_change_password` | `bool` | Optional | Whether the user must change password on next login |
| `password` | `str` | Optional | The plain text password for the user |
| `prohibit_login` | `bool` | Optional | Whether the user is prohibited from logging in |
| `restricted` | `bool` | Optional | Whether the user has restricted access privileges |
| `source_id` | `int` | Required | - |
| `visibility` | [`Visibility5`](../../doc/models/visibility-5.md) | Optional | User visibility level: public, limited, or private<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `website` | `str` | Optional | The user's personal website URL |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_user_option import EditUserOption

edit_user_option = EditUserOption(
    login_name='empty',
    source_id=66,
    active=False,
    admin=False,
    allow_create_organization=False,
    allow_git_hook=False,
    allow_import_local=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

