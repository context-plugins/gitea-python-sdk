
# Create User Option

CreateUserOption create user options

*This model accepts additional fields of type Any.*

## Structure

`CreateUserOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | For explicitly setting the user creation timestamp. Useful when users are<br>migrated from other systems. When omitted, the user's creation timestamp<br>will be set to "now". |
| `email` | `str` | Required | - |
| `full_name` | `str` | Optional | The full display name of the user |
| `login_name` | `str` | Optional | identifier of the user, provided by the external authenticator (if configured)<br><br>**Default**: `"empty"` |
| `must_change_password` | `bool` | Optional | Whether the user must change password on first login |
| `password` | `str` | Optional | The plain text password for the user |
| `restricted` | `bool` | Optional | Whether the user has restricted access privileges |
| `send_notify` | `bool` | Optional | Whether to send welcome notification email to the user |
| `source_id` | `int` | Optional | The authentication source ID to associate with the user |
| `username` | `str` | Required | username of the user |
| `visibility` | [`Visibility5`](../../doc/models/visibility-5.md) | Optional | User visibility level: public, limited, or private<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.create_user_option import CreateUserOption

create_user_option = CreateUserOption(
    email='email8',
    username='username8',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    full_name='full_name4',
    login_name='empty',
    must_change_password=False,
    password='password2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

