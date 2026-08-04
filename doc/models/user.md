
# User

User represents a user

*This model accepts additional fields of type Any.*

## Structure

`User`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active` | `bool` | Optional | Is user active |
| `avatar_url` | `str` | Optional | URL to the user's avatar |
| `created` | `datetime` | Optional | - |
| `description` | `str` | Optional | the user's description |
| `email` | `str` | Optional | - |
| `followers_count` | `int` | Optional | user counts |
| `following_count` | `int` | Optional | - |
| `full_name` | `str` | Optional | the user's full name |
| `html_url` | `str` | Optional | URL to the user's gitea page |
| `id` | `int` | Optional | the user's id |
| `is_admin` | `bool` | Optional | Is the user an administrator |
| `language` | `str` | Optional | User locale |
| `last_login` | `datetime` | Optional | - |
| `location` | `str` | Optional | the user's location |
| `login` | `str` | Optional | login of the user, same as `username` |
| `login_name` | `str` | Optional | identifier of the user, provided by the external authenticator (if configured)<br><br>**Default**: `"empty"` |
| `prohibit_login` | `bool` | Optional | Is user login prohibited |
| `restricted` | `bool` | Optional | Is user restricted |
| `source_id` | `int` | Optional | The ID of the user's Authentication Source |
| `starred_repos_count` | `int` | Optional | - |
| `visibility` | [`Visibility`](../../doc/models/visibility.md) | Optional | User visibility level option: public, limited, private<br>public UserVisibilityPublic<br>limited UserVisibilityLimited<br>private UserVisibilityPrivate |
| `website` | `str` | Optional | the user's website |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.user import User

user = User(
    active=False,
    avatar_url='avatar_url6',
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    description='description0',
    email='email6',
    login_name='empty',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

