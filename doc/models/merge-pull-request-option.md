
# Merge Pull Request Option

MergePullRequestForm form for merging Pull Request

*This model accepts additional fields of type Any.*

## Structure

`MergePullRequestOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `delete_branch_after_merge` | `bool` | Optional | - |
| `do` | [`Do`](../../doc/models/do.md) | Required | - |
| `force_merge` | `bool` | Optional | - |
| `head_commit_id` | `str` | Optional | - |
| `merge_commit_id` | `str` | Optional | - |
| `merge_message_field` | `str` | Optional | - |
| `merge_title_field` | `str` | Optional | - |
| `merge_when_checks_succeed` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.do import Do
from gitea.models.merge_pull_request_option import MergePullRequestOption

merge_pull_request_option = MergePullRequestOption(
    do=Do.REBASEMERGE,
    delete_branch_after_merge=False,
    force_merge=False,
    head_commit_id='head_commit_id6',
    merge_commit_id='merge_commit_id0',
    merge_message_field='merge_message_field8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

