
# Node Info Services

NodeInfoServices contains the third party sites this server can connect to via their application API

*This model accepts additional fields of type Any.*

## Structure

`NodeInfoServices`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inbound` | `List[str]` | Optional | Inbound lists services that can deliver content to this server |
| `outbound` | `List[str]` | Optional | Outbound lists services this server can deliver content to |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.node_info_services import NodeInfoServices

node_info_services = NodeInfoServices(
    inbound=[
        'inbound0'
    ],
    outbound=[
        'outbound9',
        'outbound0',
        'outbound1'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

