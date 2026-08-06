
# Pr Branch Info

PRBranchInfo information about a branch

*This model accepts additional fields of type Any.*

## Structure

`PrBranchInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `label` | `str` | Optional | The display name of the branch |
| `ref` | `str` | Optional | The git reference of the branch |
| `repo` | [`Repository`](../../doc/models/repository.md) | Optional | Repository represents a repository |
| `repo_id` | `int` | Optional | The unique identifier of the repository |
| `sha` | `str` | Optional | The commit SHA of the branch head |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.pr_branch_info import PrBranchInfo
from gitea.models.repository import Repository

pr_branch_info = PrBranchInfo(
    label='label4',
    ref='ref4',
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
    repo_id=8,
    sha='sha0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

