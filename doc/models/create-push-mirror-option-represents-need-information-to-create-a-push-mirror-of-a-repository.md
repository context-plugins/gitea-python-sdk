
# Create Push Mirror Option Represents Need Information to Create a Push Mirror of a Repository

*This model accepts additional fields of type Any.*

## Structure

`CreatePushMirrorOptionRepresentsNeedInformationToCreateAPushMirrorOfARepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `interval` | `str` | Optional | The sync interval for automatic updates |
| `remote_address` | `str` | Optional | The remote repository URL to push to |
| `remote_password` | `str` | Optional | The password for authentication with the remote repository |
| `remote_username` | `str` | Optional | The username for authentication with the remote repository |
| `sync_on_commit` | `bool` | Optional | Whether to sync on every commit |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_push_mirror_option_represents_need_information_to_create_a_push_mirror_of_a_repository import CreatePushMirrorOptionRepresentsNeedInformationToCreateAPushMirrorOfARepository

create_push_mirror_option_represents_need_information_to_create_a_push_mirror_of_a_repository = CreatePushMirrorOptionRepresentsNeedInformationToCreateAPushMirrorOfARepository(
    interval='interval6',
    remote_address='remote_address2',
    remote_password='remote_password2',
    remote_username='remote_username4',
    sync_on_commit=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

