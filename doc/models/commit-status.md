
# Commit Status

CommitStatus holds a single status of a single Commit

*This model accepts additional fields of type Any.*

## Structure

`CommitStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | `str` | Optional | Context is the unique context identifier for the status |
| `created_at` | `datetime` | Optional | - |
| `creator` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `description` | `str` | Optional | Description provides a brief description of the status |
| `id` | `int` | Optional | ID is the unique identifier for the commit status |
| `status` | [`Status`](../../doc/models/status.md) | Optional | State represents the status state (pending, success, error, failure)<br>pending CommitStatusPending is for when the CommitStatus is Pending<br>success CommitStatusSuccess is for when the CommitStatus is Success<br>error CommitStatusError is for when the CommitStatus is Error<br>failure CommitStatusFailure is for when the CommitStatus is Failure<br>warning CommitStatusWarning is for when the CommitStatus is Warning<br>skipped CommitStatusSkipped is for when CommitStatus is Skipped |
| `target_url` | `str` | Optional | TargetURL is the URL to link to for more details |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | URL is the API URL for this status |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.commit_status import CommitStatus
from gitea.models.user import User

commit_status = CommitStatus(
    context='context6',
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
    description='description4',
    id=204,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

