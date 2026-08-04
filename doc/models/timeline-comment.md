
# Timeline Comment

TimelineComment represents a timeline comment (comment of any type) on a commit or issue

*This model accepts additional fields of type Any.*

## Structure

`TimelineComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `assignee_team` | [`Team`](../../doc/models/team.md) | Optional | Team represents a team in an organization |
| `body` | `str` | Optional | Body contains the timeline event content |
| `created_at` | `datetime` | Optional | - |
| `dependent_issue` | [`Issue`](../../doc/models/issue.md) | Optional | Issue represents an issue in a repository |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing the comment |
| `id` | `int` | Optional | ID is the unique identifier for the timeline comment |
| `issue_url` | `str` | Optional | IssueURL is the API URL for the issue |
| `label` | [`Label`](../../doc/models/label.md) | Optional | Label a label to an issue or a pr |
| `milestone` | [`Milestone`](../../doc/models/milestone.md) | Optional | Milestone milestone is a collection of issues on one repository |
| `new_ref` | `str` | Optional | - |
| `new_title` | `str` | Optional | - |
| `old_milestone` | [`Milestone`](../../doc/models/milestone.md) | Optional | Milestone milestone is a collection of issues on one repository |
| `old_project_id` | `int` | Optional | - |
| `old_ref` | `str` | Optional | - |
| `old_title` | `str` | Optional | - |
| `project_id` | `int` | Optional | - |
| `pull_request_url` | `str` | Optional | PRURL is the API URL for the pull request (if applicable) |
| `ref_action` | `str` | Optional | - |
| `ref_comment` | [`Comment`](../../doc/models/comment.md) | Optional | Comment represents a comment on a commit or issue |
| `ref_commit_sha` | `str` | Optional | commit SHA where issue/PR was referenced |
| `ref_issue` | [`Issue`](../../doc/models/issue.md) | Optional | Issue represents an issue in a repository |
| `removed_assignee` | `bool` | Optional | whether the assignees were removed or added |
| `resolve_doer` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `review_id` | `int` | Optional | - |
| `tracked_time` | [`TrackedTime`](../../doc/models/tracked-time.md) | Optional | TrackedTime worked time for an issue / pr |
| `mtype` | `str` | Optional | Type indicates the type of timeline event |
| `updated_at` | `datetime` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.attachment import Attachment
from giteaapi.models.issue import Issue
from giteaapi.models.team import Team
from giteaapi.models.timeline_comment import TimelineComment
from giteaapi.models.user import User

timeline_comment = TimelineComment(
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
    assignee_team=Team(
        can_create_org_repo=False,
        description='description4',
        id=192,
        includes_all_repositories=False,
        name='name4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    body='body4',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    dependent_issue=Issue(
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
        body='body2',
        closed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

