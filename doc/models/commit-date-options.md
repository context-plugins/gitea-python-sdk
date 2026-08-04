
# Commit Date Options

CommitDateOptions store dates for GIT_AUTHOR_DATE and GIT_COMMITTER_DATE

*This model accepts additional fields of type Any.*

## Structure

`CommitDateOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `author` | `datetime` | Optional | - |
| `committer` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.commit_date_options import CommitDateOptions

commit_date_options = CommitDateOptions(
    author=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    committer=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

