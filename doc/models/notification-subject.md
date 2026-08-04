
# Notification Subject

NotificationSubject contains the notification subject (Issue/Pull/Commit)

*This model accepts additional fields of type Any.*

## Structure

`NotificationSubject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `html_url` | `str` | Optional | HTMLURL is the web URL for the notification subject |
| `latest_comment_html_url` | `str` | Optional | LatestCommentHTMLURL is the web URL for the latest comment |
| `latest_comment_url` | `str` | Optional | LatestCommentURL is the API URL for the latest comment |
| `state` | [`State6`](../../doc/models/state-6.md) | Optional | State indicates the current state of the notification subject<br>open NotifySubjectStateOpen is an open subject<br>closed NotifySubjectStateClosed is a closed subject<br>merged NotifySubjectStateMerged is a merged pull request |
| `title` | `str` | Optional | Title is the title of the notification subject |
| `mtype` | [`Type2`](../../doc/models/type-2.md) | Optional | Type indicates the type of the notification subject<br>Issue NotifySubjectIssue a issue is subject of an notification<br>Pull NotifySubjectPull a pull is subject of an notification<br>Commit NotifySubjectCommit a commit is subject of an notification<br>Repository NotifySubjectRepository a repository is subject of an notification |
| `url` | `str` | Optional | URL is the API URL for the notification subject |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.notification_subject import NotificationSubject
from giteaapi.models.state_6 import State6

notification_subject = NotificationSubject(
    html_url='html_url4',
    latest_comment_html_url='latest_comment_html_url4',
    latest_comment_url='latest_comment_url0',
    state=State6.MERGED,
    title='title2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

