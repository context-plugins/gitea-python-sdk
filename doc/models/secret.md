
# Secret

Secret represents a secret

*This model accepts additional fields of type Any.*

## Structure

`Secret`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `description` | `str` | Optional | the secret's description |
| `name` | `str` | Optional | the secret's name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.secret import Secret

secret = Secret(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    description='description4',
    name='name4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

