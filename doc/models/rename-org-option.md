
# Rename Org Option

RenameOrgOption options when renaming an organization

*This model accepts additional fields of type Any.*

## Structure

`RenameOrgOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `new_name` | `str` | Required | New username for this org. This name cannot be in use yet by any other user. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.rename_org_option import RenameOrgOption

rename_org_option = RenameOrgOption(
    new_name='new_name0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

