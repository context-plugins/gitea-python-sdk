
# Issue

Issue represents an issue in a repository

*This model accepts additional fields of type Any.*

## Structure

`Issue`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assets` | [`List[Attachment]`](../../doc/models/attachment.md) | Optional | - |
| `assignee` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `assignees` | [`List[User]`](../../doc/models/user.md) | Optional | - |
| `body` | `str` | Optional | - |
| `closed_at` | `datetime` | Optional | - |
| `comments` | `int` | Optional | - |
| `content_version` | `int` | Optional | The version of the issue content for optimistic locking |
| `created_at` | `datetime` | Optional | - |
| `due_date` | `datetime` | Optional | - |
| `html_url` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `is_locked` | `bool` | Optional | - |
| `labels` | [`List[Label]`](../../doc/models/label.md) | Optional | - |
| `milestone` | [`Milestone`](../../doc/models/milestone.md) | Optional | Milestone milestone is a collection of issues on one repository |
| `number` | `int` | Optional | - |
| `original_author` | `str` | Optional | - |
| `original_author_id` | `int` | Optional | - |
| `pin_order` | `int` | Optional | - |
| `projects` | [`List[Project]`](../../doc/models/project.md) | Optional | - |
| `pull_request` | [`PullRequestMeta`](../../doc/models/pull-request-meta.md) | Optional | PullRequestMeta PR info if an issue is a PR |
| `ref` | `str` | Optional | - |
| `repository` | [`RepositoryMeta`](../../doc/models/repository-meta.md) | Optional | RepositoryMeta basic repository information |
| `state` | [`State1`](../../doc/models/state-1.md) | Optional | - |
| `time_estimate` | `int` | Optional | - |
| `title` | `str` | Optional | - |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.attachment import Attachment
from gitea.models.issue import Issue
from gitea.models.user import User

issue = Issue(
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
    assignee=User(
        active=False,
        avatar_url='avatar_url4',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description2',
        email='email8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    assignees=[
        User(
            active=False,
            avatar_url='avatar_url0',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description6',
            email='email2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        User(
            active=False,
            avatar_url='avatar_url0',
            created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description6',
            email='email2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    body='body0',
    closed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

