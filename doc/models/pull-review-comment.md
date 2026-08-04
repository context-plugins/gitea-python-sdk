
# Pull Review Comment

PullReviewComment represents a comment on a pull request review

*This model accepts additional fields of type Any.*

## Structure

`PullReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `commit_id` | `str` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `diff_hunk` | `str` | Optional | - |
| `html_url` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `original_commit_id` | `str` | Optional | - |
| `original_position` | `int` | Optional | - |
| `path` | `str` | Optional | - |
| `position` | `int` | Optional | - |
| `pull_request_review_id` | `int` | Optional | - |
| `pull_request_url` | `str` | Optional | - |
| `resolver` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `updated_at` | `datetime` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.pull_review_comment import PullReviewComment

pull_review_comment = PullReviewComment(
    body='body0',
    commit_id='commit_id8',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    diff_hunk='diff_hunk8',
    html_url='html_url4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

