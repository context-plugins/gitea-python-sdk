
# General Attachment Settings

GeneralAttachmentSettings contains global Attachment settings exposed by API

*This model accepts additional fields of type Any.*

## Structure

`GeneralAttachmentSettings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `allowed_types` | `str` | Optional | AllowedTypes contains the allowed file types for attachments |
| `enabled` | `bool` | Optional | Enabled indicates if file attachments are enabled |
| `max_files` | `int` | Optional | MaxFiles is the maximum number of files per attachment |
| `max_size` | `int` | Optional | MaxSize is the maximum size for individual attachments |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.general_attachment_settings import GeneralAttachmentSettings

general_attachment_settings = GeneralAttachmentSettings(
    allowed_types='allowed_types6',
    enabled=False,
    max_files=68,
    max_size=206,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

