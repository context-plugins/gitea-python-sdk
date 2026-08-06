
# Organization Permissions

OrganizationPermissions list different users permissions on an organization

*This model accepts additional fields of type Any.*

## Structure

`OrganizationPermissions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `can_create_repository` | `bool` | Optional | Whether the user can create repositories in the organization |
| `can_read` | `bool` | Optional | Whether the user can read the organization |
| `can_write` | `bool` | Optional | Whether the user can write to the organization |
| `is_admin` | `bool` | Optional | Whether the user is an admin of the organization |
| `is_owner` | `bool` | Optional | Whether the user is an owner of the organization |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.organization_permissions import OrganizationPermissions

organization_permissions = OrganizationPermissions(
    can_create_repository=False,
    can_read=False,
    can_write=False,
    is_admin=False,
    is_owner=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

