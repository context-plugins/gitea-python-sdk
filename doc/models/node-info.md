
# Node Info

NodeInfo contains standardized way of exposing metadata about a server running one of the distributed social networks

*This model accepts additional fields of type Any.*

## Structure

`NodeInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metadata` | `Any` | Optional | Metadata contains free form key value pairs for software specific values |
| `open_registrations` | `bool` | Optional | OpenRegistrations indicates if new user registrations are accepted |
| `protocols` | `List[str]` | Optional | Protocols lists the protocols supported by this server |
| `services` | [`NodeInfoServices`](../../doc/models/node-info-services.md) | Optional | NodeInfoServices contains the third party sites this server can connect to via their application API |
| `software` | [`NodeInfoSoftware`](../../doc/models/node-info-software.md) | Optional | NodeInfoSoftware contains Metadata about server software in use |
| `usage` | [`NodeInfoUsage`](../../doc/models/node-info-usage.md) | Optional | NodeInfoUsage contains usage statistics for this server |
| `version` | `str` | Optional | Version specifies the schema version |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.node_info import NodeInfo
from gitea.models.node_info_services import NodeInfoServices
from gitea.models.node_info_software import NodeInfoSoftware

node_info = NodeInfo(
    metadata=jsonpickle.decode('{"key1":"val1","key2":"val2"}'),
    open_registrations=False,
    protocols=[
        'protocols6',
        'protocols7',
        'protocols8'
    ],
    services=NodeInfoServices(
        inbound=[
            'inbound6'
        ],
        outbound=[
            'outbound5',
            'outbound6',
            'outbound7'
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    software=NodeInfoSoftware(
        homepage='homepage0',
        name='name4',
        repository='repository6',
        version='version0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

