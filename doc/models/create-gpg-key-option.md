
# Create Gpg Key Option

CreateGPGKeyOption options create user GPG key

*This model accepts additional fields of type Any.*

## Structure

`CreateGpgKeyOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `armored_public_key` | `str` | Required | An armored GPG key to add |
| `armored_signature` | `str` | Optional | An optional armored signature for the GPG key |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_gpg_key_option import CreateGpgKeyOption

create_gpg_key_option = CreateGpgKeyOption(
    armored_public_key='armored_public_key8',
    armored_signature='armored_signature0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

