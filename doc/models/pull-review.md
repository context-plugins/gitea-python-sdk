
# Pull Review

PullReview represents a pull request review

*This model accepts additional fields of type Any.*

## Structure

`PullReview`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `comments_count` | `int` | Optional | - |
| `commit_id` | `str` | Optional | - |
| `dismissed` | `bool` | Optional | - |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing the review |
| `id` | `int` | Optional | - |
| `official` | `bool` | Optional | - |
| `pull_request_url` | `str` | Optional | HTMLPullURL is the web URL for the pull request |
| `stale` | `bool` | Optional | - |
| `state` | [`State8`](../../doc/models/state-8.md) | Optional | - |
| `submitted_at` | `datetime` | Optional | - |
| `team` | [`Team`](../../doc/models/team.md) | Optional | Team represents a team in an organization |
| `updated_at` | `datetime` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.pull_review import PullReview

pull_review = PullReview(
    body='body0',
    comments_count=72,
    commit_id='commit_id8',
    dismissed=False,
    html_url='html_url4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

