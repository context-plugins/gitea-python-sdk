
# Server Version

ServerVersion wraps the version of the server

*This model accepts additional fields of type Any.*

## Structure

`ServerVersion`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `version` | `str` | Optional | Version is the server version string |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.server_version import ServerVersion

server_version = ServerVersion(
    version='version8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

