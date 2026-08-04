
# Email

Email an email address belonging to a user

*This model accepts additional fields of type Any.*

## Structure

`Email`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `primary` | `bool` | Optional | Whether this is the primary email address |
| `user_id` | `int` | Optional | The unique identifier of the user who owns this email |
| `username` | `str` | Optional | username of the user |
| `verified` | `bool` | Optional | Whether the email address has been verified |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.email import Email

email = Email(
    email='email0',
    primary=False,
    user_id=184,
    username='username6',
    verified=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

