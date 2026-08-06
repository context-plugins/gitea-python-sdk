
# Repository

Repository represents a repository

*This model accepts additional fields of type Any.*

## Structure

`Repository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_fast_forward_only_merge` | `bool` | Optional | - |
| `allow_manual_merge` | `bool` | Optional | - |
| `allow_merge_commits` | `bool` | Optional | - |
| `allow_merge_update` | `bool` | Optional | - |
| `allow_rebase` | `bool` | Optional | - |
| `allow_rebase_explicit` | `bool` | Optional | - |
| `allow_rebase_update` | `bool` | Optional | - |
| `allow_squash_merge` | `bool` | Optional | - |
| `archived` | `bool` | Optional | - |
| `archived_at` | `datetime` | Optional | - |
| `autodetect_manual_merge` | `bool` | Optional | - |
| `avatar_url` | `str` | Optional | - |
| `branch_count` | `int` | Optional | - |
| `clone_url` | `str` | Optional | - |
| `created_at` | `datetime` | Optional | - |
| `default_allow_maintainer_edit` | `bool` | Optional | - |
| `default_branch` | `str` | Optional | - |
| `default_delete_branch_after_merge` | `bool` | Optional | - |
| `default_merge_style` | `str` | Optional | - |
| `default_target_branch` | `str` | Optional | - |
| `default_update_style` | `str` | Optional | - |
| `description` | `str` | Optional | - |
| `empty` | `bool` | Optional | - |
| `external_tracker` | [`ExternalTracker`](../../doc/models/external-tracker.md) | Optional | ExternalTracker represents settings for external tracker |
| `external_wiki` | [`ExternalWiki`](../../doc/models/external-wiki.md) | Optional | ExternalWiki represents setting for external wiki |
| `fork` | `bool` | Optional | - |
| `forks_count` | `int` | Optional | - |
| `full_name` | `str` | Optional | - |
| `has_actions` | `bool` | Optional | - |
| `has_code` | `bool` | Optional | - |
| `has_issues` | `bool` | Optional | - |
| `has_packages` | `bool` | Optional | - |
| `has_projects` | `bool` | Optional | - |
| `has_pull_requests` | `bool` | Optional | - |
| `has_releases` | `bool` | Optional | - |
| `has_wiki` | `bool` | Optional | - |
| `html_url` | `str` | Optional | - |
| `id` | `int` | Optional | - |
| `ignore_whitespace_conflicts` | `bool` | Optional | - |
| `internal` | `bool` | Optional | - |
| `internal_tracker` | [`InternalTracker`](../../doc/models/internal-tracker.md) | Optional | InternalTracker represents settings for internal tracker |
| `language` | `str` | Optional | - |
| `languages_url` | `str` | Optional | - |
| `licenses` | `List[str]` | Optional | - |
| `link` | `str` | Optional | - |
| `mirror` | `bool` | Optional | - |
| `mirror_interval` | `str` | Optional | - |
| `mirror_last_sync_at` | `datetime` | Optional | - |
| `mirror_updated` | `datetime` | Optional | - |
| `name` | `str` | Optional | - |
| `object_format_name` | [`ObjectFormatName`](../../doc/models/object-format-name.md) | Optional | ObjectFormatName of the underlying git repository<br>sha1 ObjectFormatSHA1<br>sha256 ObjectFormatSHA256 |
| `open_issues_count` | `int` | Optional | - |
| `open_pr_counter` | `int` | Optional | - |
| `original_url` | `str` | Optional | - |
| `owner` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `parent` | [`Repository`](../../doc/models/repository.md) | Optional | - |
| `permissions` | [`Permission`](../../doc/models/permission.md) | Optional | Permission represents a set of permissions |
| `private` | `bool` | Optional | - |
| `projects_mode` | `str` | Optional | - |
| `release_counter` | `int` | Optional | - |
| `repo_transfer` | [`RepoTransfer`](../../doc/models/repo-transfer.md) | Optional | RepoTransfer represents a pending repo transfer |
| `size` | `int` | Optional | - |
| `ssh_url` | `str` | Optional | - |
| `stars_count` | `int` | Optional | - |
| `template` | `bool` | Optional | - |
| `topics` | `List[str]` | Optional | - |
| `updated_at` | `datetime` | Optional | - |
| `url` | `str` | Optional | - |
| `watchers_count` | `int` | Optional | - |
| `website` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.repository import Repository

repository = Repository(
    allow_fast_forward_only_merge=False,
    allow_manual_merge=False,
    allow_merge_commits=False,
    allow_merge_update=False,
    allow_rebase=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

