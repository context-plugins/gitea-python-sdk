
# Commit Affected Files

CommitAffectedFiles store information about files affected by the commit

*This model accepts additional fields of type Any.*

## Structure

`CommitAffectedFiles`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filename` | `str` | Optional | Filename is the path of the affected file |
| `status` | `str` | Optional | Status indicates how the file was affected (added, modified, deleted) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.commit_affected_files import CommitAffectedFiles

commit_affected_files = CommitAffectedFiles(
    filename='filename2',
    status='status8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

