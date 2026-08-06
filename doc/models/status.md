
# Status

State represents the status state (pending, success, error, failure)
pending CommitStatusPending is for when the CommitStatus is Pending
success CommitStatusSuccess is for when the CommitStatus is Success
error CommitStatusError is for when the CommitStatus is Error
failure CommitStatusFailure is for when the CommitStatus is Failure
warning CommitStatusWarning is for when the CommitStatus is Warning
skipped CommitStatusSkipped is for when CommitStatus is Skipped

## Enumeration

`Status`

## Fields

| Name |
|  --- |
| `PENDING` |
| `SUCCESS` |
| `ERROR` |
| `FAILURE` |
| `WARNING` |
| `SKIPPED` |

## Example

```python
from gitea.models.status import Status

status = Status.ERROR
```

