
# Combined Status

CombinedStatus holds the combined state of several statuses for a single commit

*This model accepts additional fields of type Any.*

## Structure

`CombinedStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `commit_url` | `str` | Optional | CommitURL is the API URL for the commit |
| `repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `sha` | `str` | Optional | SHA is the commit SHA this status applies to |
| `state` | [`State`](../../doc/models/state.md) | Optional | State is the overall combined status state<br>pending CommitStatusPending is for when the CommitStatus is Pending<br>success CommitStatusSuccess is for when the CommitStatus is Success<br>error CommitStatusError is for when the CommitStatus is Error<br>failure CommitStatusFailure is for when the CommitStatus is Failure<br>warning CommitStatusWarning is for when the CommitStatus is Warning<br>skipped CommitStatusSkipped is for when CommitStatus is Skipped |
| `statuses` | [`List[CommitStatus]`](../../doc/models/commit-status.md) | Optional | Statuses contains all individual commit statuses |
| `total_count` | `int` | Optional | TotalCount is the total number of statuses |
| `url` | `str` | Optional | URL is the API URL for this combined status |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.combined_status import CombinedStatus
from gitea.models.commit_status import CommitStatus
from gitea.models.repository import Repository
from gitea.models.state import State
from gitea.models.user import User

combined_status = CombinedStatus(
    commit_url='commit_url0',
    repository=Repository(
        allow_fast_forward_only_merge=False,
        allow_manual_merge=False,
        allow_merge_commits=False,
        allow_merge_update=False,
        allow_rebase=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    sha='sha8',
    state=State.ERROR,
    statuses=[
        CommitStatus(
            context='context0',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            creator=User(
                active=False,
                avatar_url='avatar_url4',
                created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                description='description2',
                email='email8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            description='description8',
            id=216,
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

