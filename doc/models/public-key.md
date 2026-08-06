
# Public Key

PublicKey publickey is a user key to push code to repository

*This model accepts additional fields of type Any.*

## Structure

`PublicKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `fingerprint` | `str` | Optional | Fingerprint is the key's fingerprint |
| `id` | `int` | Optional | ID is the unique identifier for the public key |
| `key` | `str` | Optional | Key contains the actual SSH public key content |
| `key_type` | `str` | Optional | KeyType indicates the type of the SSH key |
| `last_used_at` | `datetime` | Optional | Updated is the time when the key was last used |
| `read_only` | `bool` | Optional | ReadOnly indicates if the key has read-only access |
| `title` | `str` | Optional | Title is the human-readable name for the key |
| `url` | `str` | Optional | URL is the API URL for this key |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.public_key import PublicKey

public_key = PublicKey(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    fingerprint='fingerprint2',
    id=168,
    key='key6',
    key_type='key_type6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

