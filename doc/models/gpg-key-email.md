
# Gpg Key Email

GPGKeyEmail an email attached to a GPGKey

*This model accepts additional fields of type Any.*

## Structure

`GpgKeyEmail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `str` | Optional | The email address associated with the GPG key |
| `verified` | `bool` | Optional | Whether the email address has been verified |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.gpg_key_email import GpgKeyEmail

gpg_key_email = GpgKeyEmail(
    email='email6',
    verified=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

