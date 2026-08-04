
# Rename Branch Repo Option

RenameBranchRepoOption options when renaming a branch in a repository

*This model accepts additional fields of type Any.*

## Structure

`RenameBranchRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Required | New branch name |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.rename_branch_repo_option import RenameBranchRepoOption

rename_branch_repo_option = RenameBranchRepoOption(
    name='name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

