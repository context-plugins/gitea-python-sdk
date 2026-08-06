
# Pull Request Meta

PullRequestMeta PR info if an issue is a PR

*This model accepts additional fields of type Any.*

## Structure

`PullRequestMeta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `draft` | `bool` | Optional | - |
| `html_url` | `str` | Optional | - |
| `merged` | `bool` | Optional | - |
| `merged_at` | `datetime` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.pull_request_meta import PullRequestMeta

pull_request_meta = PullRequestMeta(
    draft=False,
    html_url='html_url8',
    merged=False,
    merged_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

