
# Create Pull Review Comment Reply Options

CreatePullReviewCommentReplyOptions are options to reply to a pull request review comment

*This model accepts additional fields of type Any.*

## Structure

`CreatePullReviewCommentReplyOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_pull_review_comment_reply_options import CreatePullReviewCommentReplyOptions

create_pull_review_comment_reply_options = CreatePullReviewCommentReplyOptions(
    body='body2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

