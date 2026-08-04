
# Transfer Repo Option

TransferRepoOption options when transfer a repository's ownership

*This model accepts additional fields of type Any.*

## Structure

`TransferRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `new_owner` | `str` | Required | - |
| `team_ids` | `List[int]` | Optional | ID of the team or teams to add to the repository. Teams can only be added to organization-owned repositories. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.transfer_repo_option import TransferRepoOption

transfer_repo_option = TransferRepoOption(
    new_owner='new_owner6',
    team_ids=[
        3,
        4
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

