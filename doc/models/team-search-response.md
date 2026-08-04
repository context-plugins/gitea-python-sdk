
# Team Search Response

*This model accepts additional fields of type Any.*

## Structure

`TeamSearchResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Team]`](../../doc/models/team.md) | Optional | - |
| `ok` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.team import Team
from giteaapi.models.team_search_response import TeamSearchResponse

team_search_response = TeamSearchResponse(
    data=[
        Team(
            can_create_org_repo=False,
            description='description0',
            id=138,
            includes_all_repositories=False,
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Team(
            can_create_org_repo=False,
            description='description0',
            id=138,
            includes_all_repositories=False,
            name='name0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    ok=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

