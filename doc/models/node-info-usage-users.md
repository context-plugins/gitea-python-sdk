
# Node Info Usage Users

NodeInfoUsageUsers contains statistics about the users of this server

*This model accepts additional fields of type Any.*

## Structure

`NodeInfoUsageUsers`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `active_halfyear` | `int` | Optional | ActiveHalfyear is the amount of users that signed in at least once in the last 180 days |
| `active_month` | `int` | Optional | ActiveMonth is the amount of users that signed in at least once in the last 30 days |
| `total` | `int` | Optional | Total is the total amount of users on this server |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.node_info_usage_users import NodeInfoUsageUsers

node_info_usage_users = NodeInfoUsageUsers(
    active_halfyear=158,
    active_month=56,
    total=160,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

