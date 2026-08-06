
# Pull Review Request Options

PullReviewRequestOptions are options to add or remove pull request review requests

*This model accepts additional fields of type Any.*

## Structure

`PullReviewRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reviewers` | `List[str]` | Optional | - |
| `team_reviewers` | `List[str]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.pull_review_request_options import PullReviewRequestOptions

pull_review_request_options = PullReviewRequestOptions(
    reviewers=[
        'reviewers1',
        'reviewers2',
        'reviewers3'
    ],
    team_reviewers=[
        'team_reviewers3'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

