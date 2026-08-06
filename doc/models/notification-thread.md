
# Notification Thread

NotificationThread expose Notification on API

*This model accepts additional fields of type Any.*

## Structure

`NotificationThread`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Optional | ID is the unique identifier for the notification thread |
| `pinned` | `bool` | Optional | Pinned indicates if the notification is pinned |
| `repository` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `subject` | [`NotificationSubject`](../../doc/models/notification-subject.md) | Optional | NotificationSubject contains the notification subject (Issue/Pull/Commit) |
| `unread` | `bool` | Optional | Unread indicates if the notification has been read |
| `updated_at` | `datetime` | Optional | UpdatedAt is the time when the notification was last updated |
| `url` | `str` | Optional | URL is the API URL for this notification thread |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.notification_subject import NotificationSubject
from gitea.models.notification_thread import NotificationThread
from gitea.models.repository import Repository
from gitea.models.state_6 import State6

notification_thread = NotificationThread(
    id=106,
    pinned=False,
    repository=Repository(
        allow_fast_forward_only_merge=False,
        allow_manual_merge=False,
        allow_merge_commits=False,
        allow_merge_update=False,
        allow_rebase=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    subject=NotificationSubject(
        html_url='html_url4',
        latest_comment_html_url='latest_comment_html_url4',
        latest_comment_url='latest_comment_url0',
        state=State6.OPEN,
        title='title8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    unread=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

