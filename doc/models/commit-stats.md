
# Commit Stats

CommitStats is statistics for a RepoCommit

*This model accepts additional fields of type Any.*

## Structure

`CommitStats`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additions` | `int` | Optional | Additions is the number of lines added |
| `deletions` | `int` | Optional | Deletions is the number of lines deleted |
| `total` | `int` | Optional | Total is the total number of lines changed |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.commit_stats import CommitStats

commit_stats = CommitStats(
    additions=80,
    deletions=164,
    total=212,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

