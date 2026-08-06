
# Node Info Usage

NodeInfoUsage contains usage statistics for this server

*This model accepts additional fields of type Any.*

## Structure

`NodeInfoUsage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `local_comments` | `int` | Optional | LocalComments is the total amount of comments made by users local to this server |
| `local_posts` | `int` | Optional | LocalPosts is the total amount of posts made by users local to this server |
| `users` | [`NodeInfoUsageUsers`](../../doc/models/node-info-usage-users.md) | Optional | NodeInfoUsageUsers contains statistics about the users of this server |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.node_info_usage import NodeInfoUsage
from gitea.models.node_info_usage_users import NodeInfoUsageUsers

node_info_usage = NodeInfoUsage(
    local_comments=184,
    local_posts=222,
    users=NodeInfoUsageUsers(
        active_halfyear=190,
        active_month=88,
        total=64,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

