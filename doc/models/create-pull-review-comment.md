
# Create Pull Review Comment

CreatePullReviewComment represent a review comment for creation api

*This model accepts additional fields of type Any.*

## Structure

`CreatePullReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `new_position` | `int` | Optional | if comment to new file line or 0 |
| `old_position` | `int` | Optional | if comment to old file line or 0 |
| `path` | `str` | Optional | the tree path |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_pull_review_comment import CreatePullReviewComment

create_pull_review_comment = CreatePullReviewComment(
    body='body4',
    new_position=174,
    old_position=100,
    path='path2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

