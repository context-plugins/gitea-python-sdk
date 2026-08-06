
# Stop Watch

StopWatch represent a running stopwatch

*This model accepts additional fields of type Any.*

## Structure

`StopWatch`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | - |
| `duration` | `str` | Optional | Duration is a human-readable duration string |
| `issue_index` | `int` | Optional | IssueIndex is the index number of the associated issue |
| `issue_title` | `str` | Optional | IssueTitle is the title of the associated issue |
| `repo_name` | `str` | Optional | RepoName is the name of the repository |
| `repo_owner_name` | `str` | Optional | RepoOwnerName is the name of the repository owner |
| `seconds` | `int` | Optional | Seconds is the total elapsed time in seconds |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.stop_watch import StopWatch

stop_watch = StopWatch(
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    duration='duration2',
    issue_index=42,
    issue_title='issue_title8',
    repo_name='repo_name0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

