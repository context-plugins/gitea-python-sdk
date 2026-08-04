
# Create Status Option

CreateStatusOption holds the information needed to create a new CommitStatus for a Commit

*This model accepts additional fields of type Any.*

## Structure

`CreateStatusOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `context` | `str` | Optional | Context is the unique context identifier for the status |
| `description` | `str` | Optional | Description provides a brief description of the status |
| `state` | [`State2`](../../doc/models/state-2.md) | Optional | State represents the status state to set (pending, success, error, failure)<br>pending CommitStatusPending is for when the CommitStatus is Pending<br>success CommitStatusSuccess is for when the CommitStatus is Success<br>error CommitStatusError is for when the CommitStatus is Error<br>failure CommitStatusFailure is for when the CommitStatus is Failure<br>warning CommitStatusWarning is for when the CommitStatus is Warning<br>skipped CommitStatusSkipped is for when CommitStatus is Skipped |
| `target_url` | `str` | Optional | TargetURL is the URL to link to for more details |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_status_option import CreateStatusOption
from giteaapi.models.state_2 import State2

create_status_option = CreateStatusOption(
    context='context0',
    description='description8',
    state=State2.ERROR,
    target_url='target_url6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

