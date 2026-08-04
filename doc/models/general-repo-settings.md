
# General Repo Settings

GeneralRepoSettings contains global repository settings exposed by API

*This model accepts additional fields of type Any.*

## Structure

`GeneralRepoSettings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `http_git_disabled` | `bool` | Optional | HTTPGitDisabled indicates if HTTP Git operations are disabled |
| `lfs_disabled` | `bool` | Optional | LFSDisabled indicates if Git LFS support is disabled |
| `migrations_disabled` | `bool` | Optional | MigrationsDisabled indicates if repository migrations are disabled |
| `mirrors_disabled` | `bool` | Optional | MirrorsDisabled indicates if repository mirroring is disabled |
| `stars_disabled` | `bool` | Optional | StarsDisabled indicates if repository starring is disabled |
| `time_tracking_disabled` | `bool` | Optional | TimeTrackingDisabled indicates if time tracking is disabled |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.general_repo_settings import GeneralRepoSettings

general_repo_settings = GeneralRepoSettings(
    http_git_disabled=False,
    lfs_disabled=False,
    migrations_disabled=False,
    mirrors_disabled=False,
    stars_disabled=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

