
# Pull Request

PullRequest represents a pull request

*This model accepts additional fields of type Any.*

## Structure

`PullRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additions` | `int` | Optional | The number of lines added in the pull request |
| `allow_maintainer_edit` | `bool` | Optional | Whether maintainers can edit the pull request |
| `assignee` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `assignees` | [`List[User]`](../../doc/models/user.md) | Optional | The list of users assigned to the pull request |
| `base` | [`PrBranchInfo`](../../doc/models/pr-branch-info.md) | Optional | PRBranchInfo information about a branch |
| `body` | `str` | Optional | The description body of the pull request |
| `changed_files` | `int` | Optional | The number of files changed in the pull request |
| `closed_at` | `datetime` | Optional | - |
| `comments` | `int` | Optional | The number of comments on the pull request |
| `content_version` | `int` | Optional | The version of the pull request content for optimistic locking |
| `created_at` | `datetime` | Optional | - |
| `deletions` | `int` | Optional | The number of lines deleted in the pull request |
| `diff_url` | `str` | Optional | The URL to download the diff patch |
| `draft` | `bool` | Optional | Whether the pull request is a draft |
| `due_date` | `datetime` | Optional | - |
| `head` | [`PrBranchInfo`](../../doc/models/pr-branch-info.md) | Optional | PRBranchInfo information about a branch |
| `html_url` | `str` | Optional | The HTML URL to view the pull request |
| `id` | `int` | Optional | The unique identifier of the pull request |
| `is_locked` | `bool` | Optional | Whether the pull request conversation is locked |
| `labels` | [`List[Label]`](../../doc/models/label.md) | Optional | The labels attached to the pull request |
| `merge_base` | `str` | Optional | The merge base commit SHA |
| `merge_commit_sha` | `str` | Optional | The SHA of the merge commit |
| `mergeable` | `bool` | Optional | Whether the pull request can be merged |
| `merged` | `bool` | Optional | Whether the pull request has been merged |
| `merged_at` | `datetime` | Optional | - |
| `merged_by` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `milestone` | [`Milestone`](../../doc/models/milestone.md) | Optional | Milestone milestone is a collection of issues on one repository |
| `number` | `int` | Optional | The pull request number |
| `patch_url` | `str` | Optional | The URL to download the patch file |
| `pin_order` | `int` | Optional | The pin order for the pull request |
| `requested_reviewers` | [`List[User]`](../../doc/models/user.md) | Optional | The users requested to review the pull request |
| `requested_reviewers_teams` | [`List[Team]`](../../doc/models/team.md) | Optional | The teams requested to review the pull request |
| `review_comments` | `int` | Optional | number of review comments made on the diff of a PR review (not including comments on commits or issues in a PR) |
| `state` | [`State7`](../../doc/models/state-7.md) | Optional | The current state of the pull request<br>open StateOpen pr is opened<br>closed StateClosed pr is closed |
| `title` | `str` | Optional | The title of the pull request |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | The API URL of the pull request |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.pr_branch_info import PrBranchInfo
from gitea.models.pull_request import PullRequest
from gitea.models.repository import Repository
from gitea.models.user import User

pull_request = PullRequest(
    additions=160,
    allow_maintainer_edit=False,
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
    base=PrBranchInfo(
        label='label6',
        ref='ref6',
        repo=Repository(
            allow_fast_forward_only_merge=False,
            allow_manual_merge=False,
            allow_merge_commits=False,
            allow_merge_update=False,
            allow_rebase=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        repo_id=26,
        sha='sha2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

