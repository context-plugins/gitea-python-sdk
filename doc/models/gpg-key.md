
# Gpg Key

GPGKey a user GPG key to sign commit and tag in repository

*This model accepts additional fields of type Any.*

## Structure

`GpgKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `can_certify` | `bool` | Optional | Whether the key can be used for certification |
| `can_encrypt_comms` | `bool` | Optional | Whether the key can be used for encrypting communications |
| `can_encrypt_storage` | `bool` | Optional | Whether the key can be used for encrypting storage |
| `can_sign` | `bool` | Optional | Whether the key can be used for signing |
| `created_at` | `datetime` | Optional | - |
| `emails` | [`List[GpgKeyEmail]`](../../doc/models/gpg-key-email.md) | Optional | List of email addresses associated with this GPG key |
| `expires_at` | `datetime` | Optional | - |
| `id` | `int` | Optional | The unique identifier of the GPG key |
| `key_id` | `str` | Optional | The key ID of the GPG key |
| `primary_key_id` | `str` | Optional | The primary key ID of the GPG key |
| `public_key` | `str` | Optional | The public key content in armored format |
| `subkeys` | [`List[GpgKey]`](../../doc/models/gpg-key.md) | Optional | List of subkeys of this GPG key |
| `verified` | `bool` | Optional | Whether the GPG key has been verified |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.gpg_key import GpgKey

gpg_key = GpgKey(
    can_certify=False,
    can_encrypt_comms=False,
    can_encrypt_storage=False,
    can_sign=False,
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

