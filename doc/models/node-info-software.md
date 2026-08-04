
# Node Info Software

NodeInfoSoftware contains Metadata about server software in use

*This model accepts additional fields of type Any.*

## Structure

`NodeInfoSoftware`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `homepage` | `str` | Optional | Homepage is the URL to the homepage of this server software |
| `name` | `str` | Optional | Name is the canonical name of this server software |
| `repository` | `str` | Optional | Repository is the URL to the source code repository |
| `version` | `str` | Optional | Version is the version of this server software |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.node_info_software import NodeInfoSoftware

node_info_software = NodeInfoSoftware(
    homepage='homepage8',
    name='name2',
    repository='repository2',
    version='version8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

