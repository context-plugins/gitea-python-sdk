
# Comment

Comment represents a comment on a commit or issue

*This model accepts additional fields of type Any.*

## Structure

`Comment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assets` | [`List[Attachment]`](../../doc/models/attachment.md) | Optional | Attachments contains files attached to the comment |
| `body` | `str` | Optional | Body contains the comment text content |
| `created_at` | `datetime` | Optional | - |
| `html_url` | `str` | Optional | HTMLURL is the web URL for viewing the comment |
| `id` | `int` | Optional | ID is the unique identifier for the comment |
| `issue_url` | `str` | Optional | IssueURL is the API URL for the issue |
| `original_author` | `str` | Optional | OriginalAuthor is the original author name (for imported comments) |
| `original_author_id` | `int` | Optional | OriginalAuthorID is the original author ID (for imported comments) |
| `pull_request_url` | `str` | Optional | PRURL is the API URL for the pull request (if applicable) |
| `updated_at` | `datetime` | Optional | - |
| `user` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.attachment import Attachment
from giteaapi.models.comment import Comment

comment = Comment(
    assets=[
        Attachment(
            browser_download_url='browser_download_url6',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            download_count=224,
            id=12,
            name='name8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Attachment(
            browser_download_url='browser_download_url6',
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            download_count=224,
            id=12,
            name='name8',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    body='body2',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    html_url='html_url4',
    id=100,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

