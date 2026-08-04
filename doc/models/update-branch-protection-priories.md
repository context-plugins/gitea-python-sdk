
# Update Branch Protection Priories

UpdateBranchProtectionPriories a list to update the branch protection rule priorities

*This model accepts additional fields of type Any.*

## Structure

`UpdateBranchProtectionPriories`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `List[int]` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.update_branch_protection_priories import UpdateBranchProtectionPriories

update_branch_protection_priories = UpdateBranchProtectionPriories(
    ids=[
        41,
        42
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

