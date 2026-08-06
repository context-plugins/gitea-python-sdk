
# Activity

*This model accepts additional fields of type Any.*

## Structure

`Activity`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `act_user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `act_user_id` | `int` | Optional | The ID of the user who performed the action |
| `comment` | [`Comment`](../../doc/models/comment.md) | Optional | Comment represents a comment on a commit or issue |
| `comment_id` | `int` | Optional | The ID of the comment associated with the activity (if applicable) |
| `content` | `str` | Optional | Additional content or details about the activity |
| `created` | `datetime` | Optional | The date and time when the activity occurred |
| `id` | `int` | Optional | The unique identifier of the activity |
| `is_private` | `bool` | Optional | Whether this activity is from a private repository |
| `op_type` | [`OpType`](../../doc/models/op-type.md) | Optional | the type of action |
| `ref_name` | `str` | Optional | The name of the git reference (branch/tag) associated with the activity |
| `repo` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `repo_id` | `int` | Optional | The ID of the repository associated with the activity |
| `user_id` | `int` | Optional | The ID of the user who receives/sees this activity |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.activity import Activity
from gitea.models.attachment import Attachment
from gitea.models.comment import Comment
from gitea.models.user import User

activity = Activity(
    act_user=User(
        active=False,
        avatar_url='avatar_url4',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description2',
        email='email8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    act_user_id=18,
    comment=Comment(
        assets=[
            Attachment(
                browser_download_url='browser_download_url6',
                created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                download_count=224,
                id=12,
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Attachment(
                browser_download_url='browser_download_url6',
                created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                download_count=224,
                id=12,
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        body='body2',
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        html_url='html_url4',
        id=100,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    comment_id=0,
    content='content2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

