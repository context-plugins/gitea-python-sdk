
# Create Pull Request Option

CreatePullRequestOption options when creating a pull request

*This model accepts additional fields of type Any.*

## Structure

`CreatePullRequestOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_maintainer_edit` | `bool` | Optional | Whether maintainers can edit the pull request |
| `assignee` | `str` | Optional | The primary assignee username |
| `assignees` | `List[str]` | Optional | The list of assignee usernames |
| `base` | `str` | Optional | The base branch for the pull request |
| `body` | `str` | Optional | The description body of the pull request |
| `due_date` | `datetime` | Optional | - |
| `head` | `str` | Optional | The head branch for the pull request, it could be a branch name on the base repository or<br>a form like `<username>:<branch>` which refers to the user's fork repository's branch. |
| `labels` | `List[int]` | Optional | The list of label IDs to assign to the pull request |
| `milestone` | `int` | Optional | The milestone ID to assign to the pull request |
| `reviewers` | `List[str]` | Optional | The list of reviewer usernames |
| `team_reviewers` | `List[str]` | Optional | The list of team reviewer names |
| `title` | `str` | Optional | The title of the pull request |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_pull_request_option import CreatePullRequestOption

create_pull_request_option = CreatePullRequestOption(
    allow_maintainer_edit=False,
    assignee='assignee6',
    assignees=[
        'assignees5',
        'assignees6'
    ],
    base='base0',
    body='body0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

