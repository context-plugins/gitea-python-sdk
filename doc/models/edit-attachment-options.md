
# Edit Attachment Options

EditAttachmentOptions options for editing attachments

*This model accepts additional fields of type Any.*

## Structure

`EditAttachmentOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | Name is the new filename for the attachment |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.edit_attachment_options import EditAttachmentOptions

edit_attachment_options = EditAttachmentOptions(
    name='name6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

