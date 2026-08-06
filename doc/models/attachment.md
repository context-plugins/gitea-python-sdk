
# Attachment

Attachment a generic attachment

*This model accepts additional fields of type Any.*

## Structure

`Attachment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `browser_download_url` | `str` | Optional | DownloadURL is the URL to download the attachment |
| `created_at` | `datetime` | Optional | - |
| `download_count` | `int` | Optional | DownloadCount is the number of times the attachment has been downloaded |
| `id` | `int` | Optional | ID is the unique identifier for the attachment |
| `name` | `str` | Optional | Name is the filename of the attachment |
| `size` | `int` | Optional | Size is the file size in bytes |
| `uuid` | `str` | Optional | UUID is the unique identifier for the attachment file |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.attachment import Attachment

attachment = Attachment(
    browser_download_url='browser_download_url6',
    created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    download_count=204,
    id=248,
    name='name8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

