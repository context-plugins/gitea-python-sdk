
# Create Branch Protection Option

CreateBranchProtectionOption options for creating a branch protection

*This model accepts additional fields of type Any.*

## Structure

`CreateBranchProtectionOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `approvals_whitelist_teams` | `List[str]` | Optional | - |
| `approvals_whitelist_username` | `List[str]` | Optional | - |
| `block_admin_merge_override` | `bool` | Optional | - |
| `block_on_official_review_requests` | `bool` | Optional | - |
| `block_on_outdated_branch` | `bool` | Optional | - |
| `block_on_rejected_reviews` | `bool` | Optional | - |
| `branch_name` | `str` | Optional | Deprecated: true |
| `bypass_allowlist_teams` | `List[str]` | Optional | - |
| `bypass_allowlist_usernames` | `List[str]` | Optional | - |
| `dismiss_stale_approvals` | `bool` | Optional | - |
| `enable_approvals_whitelist` | `bool` | Optional | - |
| `enable_bypass_allowlist` | `bool` | Optional | - |
| `enable_force_push` | `bool` | Optional | - |
| `enable_force_push_allowlist` | `bool` | Optional | - |
| `enable_merge_whitelist` | `bool` | Optional | - |
| `enable_push` | `bool` | Optional | - |
| `enable_push_whitelist` | `bool` | Optional | - |
| `enable_status_check` | `bool` | Optional | - |
| `force_push_allowlist_deploy_keys` | `bool` | Optional | - |
| `force_push_allowlist_teams` | `List[str]` | Optional | - |
| `force_push_allowlist_usernames` | `List[str]` | Optional | - |
| `ignore_stale_approvals` | `bool` | Optional | - |
| `merge_whitelist_teams` | `List[str]` | Optional | - |
| `merge_whitelist_usernames` | `List[str]` | Optional | - |
| `priority` | `int` | Optional | - |
| `protected_file_patterns` | `str` | Optional | - |
| `push_whitelist_deploy_keys` | `bool` | Optional | - |
| `push_whitelist_teams` | `List[str]` | Optional | - |
| `push_whitelist_usernames` | `List[str]` | Optional | - |
| `require_signed_commits` | `bool` | Optional | - |
| `required_approvals` | `int` | Optional | - |
| `rule_name` | `str` | Optional | - |
| `status_check_contexts` | `List[str]` | Optional | - |
| `unprotected_file_patterns` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.create_branch_protection_option import CreateBranchProtectionOption

create_branch_protection_option = CreateBranchProtectionOption(
    approvals_whitelist_teams=[
        'approvals_whitelist_teams2'
    ],
    approvals_whitelist_username=[
        'approvals_whitelist_username1',
        'approvals_whitelist_username2',
        'approvals_whitelist_username3'
    ],
    block_admin_merge_override=False,
    block_on_official_review_requests=False,
    block_on_outdated_branch=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

