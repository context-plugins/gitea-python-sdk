
# Deploy Key

DeployKey a deploy key

*This model accepts additional fields of type Any.*

## Structure

`DeployKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional | - |
| `fingerprint` | `str` | Optional | Fingerprint is the key's fingerprint |
| `id` | `int` | Optional | ID is the unique identifier for the deploy key |
| `key` | `str` | Optional | Key contains the actual SSH key content |
| `key_id` | `int` | Optional | KeyID is the associated public key ID |
| `read_only` | `bool` | Optional | ReadOnly indicates if the key has read-only access |
| `repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `title` | `str` | Optional | Title is the human-readable name for the key |
| `url` | `str` | Optional | URL is the API URL for this deploy key |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.deploy_key import DeployKey

deploy_key = DeployKey(
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    fingerprint='fingerprint0',
    id=92,
    key='key4',
    key_id=76,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

