
# Edit Pull Request Option

EditPullRequestOption options when modify pull request

*This model accepts additional fields of type Any.*

## Structure

`EditPullRequestOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_maintainer_edit` | `bool` | Optional | Whether to allow maintainer edits |
| `assignee` | `str` | Optional | The new primary assignee username |
| `assignees` | `List[str]` | Optional | The new list of assignee usernames |
| `base` | `str` | Optional | The new base branch for the pull request |
| `body` | `str` | Optional | The new description body for the pull request |
| `content_version` | `int` | Optional | The current version of the pull request content to detect conflicts during editing |
| `due_date` | `datetime` | Optional | - |
| `labels` | `List[int]` | Optional | The new list of label IDs for the pull request |
| `milestone` | `int` | Optional | The new milestone ID for the pull request |
| `state` | `str` | Optional | The new state for the pull request |
| `title` | `str` | Optional | The new title for the pull request |
| `unset_due_date` | `bool` | Optional | Whether to remove the current deadline |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_pull_request_option import EditPullRequestOption

edit_pull_request_option = EditPullRequestOption(
    allow_maintainer_edit=False,
    assignee='assignee6',
    assignees=[
        'assignees5'
    ],
    base='base0',
    body='body0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

