
# Create Key Option

CreateKeyOption options when creating a key

*This model accepts additional fields of type Any.*

## Structure

`CreateKeyOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `str` | Required | An armored SSH key to add |
| `read_only` | `bool` | Optional | Describe if the key has only read access or read/write |
| `title` | `str` | Required | Title of the key to add |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_key_option import CreateKeyOption

create_key_option = CreateKeyOption(
    key='key8',
    title='title6',
    read_only=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

