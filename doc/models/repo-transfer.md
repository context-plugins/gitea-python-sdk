
# Repo Transfer

RepoTransfer represents a pending repo transfer

*This model accepts additional fields of type Any.*

## Structure

`RepoTransfer`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `doer` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `recipient` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `teams` | [`List[Team]`](../../doc/models/team.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.repo_transfer import RepoTransfer
from gitea.models.team import Team
from gitea.models.user import User

repo_transfer = RepoTransfer(
    doer=User(
        active=False,
        avatar_url='avatar_url2',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description6',
        email='email0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    recipient=User(
        active=False,
        avatar_url='avatar_url4',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description2',
        email='email8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    teams=[
        Team(
            can_create_org_repo=False,
            description='description8',
            id=82,
            includes_all_repositories=False,
            name='name8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

