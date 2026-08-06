
# Edit Issue Comment Option

EditIssueCommentOption options for editing a comment

*This model accepts additional fields of type Any.*

## Structure

`EditIssueCommentOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_issue_comment_option import EditIssueCommentOption

edit_issue_comment_option = EditIssueCommentOption(
    body='body8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

