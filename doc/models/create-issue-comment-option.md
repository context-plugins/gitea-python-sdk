
# Create Issue Comment Option

CreateIssueCommentOption options for creating a comment on an issue

*This model accepts additional fields of type Any.*

## Structure

`CreateIssueCommentOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | `str` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_issue_comment_option import CreateIssueCommentOption

create_issue_comment_option = CreateIssueCommentOption(
    body='body8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

