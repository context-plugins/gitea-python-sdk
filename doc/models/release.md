
# Release

Release represents a repository release

*This model accepts additional fields of type Any.*

## Structure

`Release`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assets` | [`List[Attachment]`](../../doc/models/attachment.md) | Optional | The files attached to the release |
| `author` | [`User`](../../doc/models/user.md) | Optional | User represents a user |
| `body` | `str` | Optional | The release notes or description |
| `created_at` | `datetime` | Optional | - |
| `draft` | `bool` | Optional | Whether the release is a draft |
| `html_url` | `str` | Optional | The HTML URL to view the release |
| `id` | `int` | Optional | The unique identifier of the release |
| `name` | `str` | Optional | The display title of the release |
| `prerelease` | `bool` | Optional | Whether the release is a prerelease |
| `published_at` | `datetime` | Optional | - |
| `tag_name` | `str` | Optional | The name of the git tag associated with the release |
| `tarball_url` | `str` | Optional | The URL to download the tarball archive |
| `target_commitish` | `str` | Optional | The target commitish for the release |
| `upload_url` | `str` | Optional | The URL template for uploading release assets |
| `url` | `str` | Optional | The API URL of the release |
| `zipball_url` | `str` | Optional | The URL to download the zip archive |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.attachment import Attachment
from giteaapi.models.release import Release
from giteaapi.models.user import User

release = Release(
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
    author=User(
        active=False,
        avatar_url='avatar_url6',
        created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        description='description0',
        email='email6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    body='body8',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    draft=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

