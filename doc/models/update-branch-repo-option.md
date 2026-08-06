
# Update Branch Repo Option

UpdateBranchRepoOption options when updating a branch reference in a repository

*This model accepts additional fields of type Any.*

## Structure

`UpdateBranchRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `force` | `bool` | Optional | Force update even if the change is not a fast-forward |
| `new_commit_id` | `str` | Required | New commit SHA (or any ref) the branch should point to |
| `old_commit_id` | `str` | Optional | Expected old commit SHA of the branch; if provided it must match the current tip |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.update_branch_repo_option import UpdateBranchRepoOption

update_branch_repo_option = UpdateBranchRepoOption(
    new_commit_id='new_commit_id8',
    force=False,
    old_commit_id='old_commit_id2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

