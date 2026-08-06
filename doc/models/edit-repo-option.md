
# Edit Repo Option

EditRepoOption options when editing a repository's properties

*This model accepts additional fields of type Any.*

## Structure

`EditRepoOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allow_fast_forward_only_merge` | `bool` | Optional | either `true` to allow fast-forward-only merging pull requests, or `false` to prevent fast-forward-only merging. |
| `allow_manual_merge` | `bool` | Optional | either `true` to allow mark pr as merged manually, or `false` to prevent it. |
| `allow_merge_commits` | `bool` | Optional | either `true` to allow merging pull requests with a merge commit, or `false` to prevent merging pull requests with merge commits. |
| `allow_merge_update` | `bool` | Optional | either `true` to allow updating pull request branch by merge, or `false` to prevent it. |
| `allow_rebase` | `bool` | Optional | either `true` to allow rebase-merging pull requests, or `false` to prevent rebase-merging. |
| `allow_rebase_explicit` | `bool` | Optional | either `true` to allow rebase with explicit merge commits (--no-ff), or `false` to prevent rebase with explicit merge commits. |
| `allow_rebase_update` | `bool` | Optional | either `true` to allow updating pull request branch by rebase, or `false` to prevent it. |
| `allow_squash_merge` | `bool` | Optional | either `true` to allow squash-merging pull requests, or `false` to prevent squash-merging. |
| `archived` | `bool` | Optional | set to `true` to archive this repository. |
| `autodetect_manual_merge` | `bool` | Optional | either `true` to enable AutodetectManualMerge, or `false` to prevent it. Note: In some special cases, misjudgments can occur. |
| `default_allow_maintainer_edit` | `bool` | Optional | set to `true` to allow edits from maintainers by default |
| `default_branch` | `str` | Optional | sets the default branch for this repository. |
| `default_delete_branch_after_merge` | `bool` | Optional | set to `true` to delete pr branch after merge by default |
| `default_merge_style` | `str` | Optional | set to a merge style to be used by this repository: "merge", "rebase", "rebase-merge", "squash", or "fast-forward-only". |
| `default_update_style` | `str` | Optional | set to an update style to be used by this repository: "merge" or "rebase". |
| `description` | `str` | Optional | a short description of the repository. |
| `enable_prune` | `bool` | Optional | enable prune - remove obsolete remote-tracking references when mirroring |
| `external_tracker` | [`ExternalTracker`](../../doc/models/external-tracker.md) | Optional | ExternalTracker represents settings for external tracker |
| `external_wiki` | [`ExternalWiki`](../../doc/models/external-wiki.md) | Optional | ExternalWiki represents setting for external wiki |
| `has_actions` | `bool` | Optional | either `true` to enable actions unit, or `false` to disable them. |
| `has_code` | `bool` | Optional | either `true` to enable code for this repository or `false` to disable it. |
| `has_issues` | `bool` | Optional | either `true` to enable issues for this repository or `false` to disable them. |
| `has_packages` | `bool` | Optional | either `true` to enable packages unit, or `false` to disable them. |
| `has_projects` | `bool` | Optional | either `true` to enable project unit, or `false` to disable them. |
| `has_pull_requests` | `bool` | Optional | either `true` to allow pull requests, or `false` to prevent pull request. |
| `has_releases` | `bool` | Optional | either `true` to enable releases unit, or `false` to disable them. |
| `has_wiki` | `bool` | Optional | either `true` to enable the wiki for this repository or `false` to disable it. |
| `ignore_whitespace_conflicts` | `bool` | Optional | either `true` to ignore whitespace for conflicts, or `false` to not ignore whitespace. |
| `internal_tracker` | [`InternalTracker`](../../doc/models/internal-tracker.md) | Optional | InternalTracker represents settings for internal tracker |
| `mirror_interval` | `str` | Optional | set to a string like `8h30m0s` to set the mirror interval time |
| `mirror_password` | `str` | Optional | authentication password for the remote repository (mirrors) |
| `mirror_token` | `str` | Optional | authentication token for the remote repository (mirrors) |
| `mirror_username` | `str` | Optional | authentication username for the remote repository (mirrors) |
| `name` | `str` | Optional | name of the repository |
| `private` | `bool` | Optional | either `true` to make the repository private or `false` to make it public.<br>Note: you will get a 422 error if the organization restricts changing repository visibility to organization<br>owners and a non-owner tries to change the value of private. |
| `projects_mode` | `str` | Optional | `repo` to only allow repo-level projects, `owner` to only allow owner projects, `all` to allow both. |
| `template` | `bool` | Optional | either `true` to make this repository a template or `false` to make it a normal repository |
| `website` | `str` | Optional | a URL with more information about the repository. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_repo_option import EditRepoOption

edit_repo_option = EditRepoOption(
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

