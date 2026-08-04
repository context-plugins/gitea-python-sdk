
# Create Pull Review Options

CreatePullReviewOptions are options to create a pull request review

*This model accepts additional fields of type Any.*

## Structure

`CreatePullReviewOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Optional | - |
| `comments` | [`List[CreatePullReviewComment]`](../../doc/models/create-pull-review-comment.md) | Optional | - |
| `commit_id` | `str` | Optional | - |
| `event` | [`Event`](../../doc/models/event.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_pull_review_comment import CreatePullReviewComment
from giteaapi.models.create_pull_review_options import CreatePullReviewOptions
from giteaapi.models.event import Event

create_pull_review_options = CreatePullReviewOptions(
    body='body2',
    comments=[
        CreatePullReviewComment(
            body='body4',
            new_position=216,
            old_position=114,
            path='path2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        CreatePullReviewComment(
            body='body4',
            new_position=216,
            old_position=114,
            path='path2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        CreatePullReviewComment(
            body='body4',
            new_position=216,
            old_position=114,
            path='path2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    commit_id='commit_id0',
    event=Event.PENDING,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

