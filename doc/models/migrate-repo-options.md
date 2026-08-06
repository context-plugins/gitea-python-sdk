
# Migrate Repo Options

MigrateRepoOptions options for migrating repository's
this is used to interact with api v1

*This model accepts additional fields of type Any.*

## Structure

`MigrateRepoOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `auth_password` | `str` | Optional | - |
| `auth_token` | `str` | Optional | - |
| `auth_username` | `str` | Optional | - |
| `aws_access_key_id` | `str` | Optional | - |
| `aws_secret_access_key` | `str` | Optional | - |
| `clone_addr` | `str` | Required | - |
| `description` | `str` | Optional | - |
| `issues` | `bool` | Optional | - |
| `labels` | `bool` | Optional | - |
| `lfs` | `bool` | Optional | - |
| `lfs_endpoint` | `str` | Optional | - |
| `milestones` | `bool` | Optional | - |
| `mirror` | `bool` | Optional | - |
| `mirror_interval` | `str` | Optional | - |
| `private` | `bool` | Optional | - |
| `pull_requests` | `bool` | Optional | - |
| `releases` | `bool` | Optional | - |
| `repo_name` | `str` | Required | - |
| `repo_owner` | `str` | Optional | the organization's name or individual user's name who will own the migrated repository |
| `service` | [`Service`](../../doc/models/service.md) | Optional | - |
| `uid` | `int` | Optional | deprecated (only for backwards compatibility, use repo_owner instead) |
| `wiki` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.migrate_repo_options import MigrateRepoOptions

migrate_repo_options = MigrateRepoOptions(
    clone_addr='clone_addr0',
    repo_name='repo_name0',
    auth_password='auth_password2',
    auth_token='auth_token2',
    auth_username='auth_username4',
    aws_access_key_id='aws_access_key_id8',
    aws_secret_access_key='aws_secret_access_key0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

