
# Create Branch Repo Option

CreateBranchRepoOption options when creating a branch in a repository

*This model accepts additional fields of type Any.*

## Structure

`CreateBranchRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `new_branch_name` | `str` | Required | Name of the branch to create |
| `old_branch_name` | `str` | Optional | Deprecated: true<br>Name of the old branch to create from |
| `old_ref_name` | `str` | Optional | Name of the old branch/tag/commit to create from |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_branch_repo_option import CreateBranchRepoOption

create_branch_repo_option = CreateBranchRepoOption(
    new_branch_name='new_branch_name4',
    old_branch_name='old_branch_name8',
    old_ref_name='old_ref_name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

