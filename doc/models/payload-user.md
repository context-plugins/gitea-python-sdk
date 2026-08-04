
# Payload User

PayloadUser represents the author or committer of a commit

*This model accepts additional fields of type Any.*

## Structure

`PayloadUser`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | - |
| `name` | `str` | Optional | Full name of the commit author |
| `username` | `str` | Optional | username of the user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.payload_user import PayloadUser

payload_user = PayloadUser(
    email='email4',
    name='name2',
    username='username8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

