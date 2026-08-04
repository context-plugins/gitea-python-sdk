
# Change File Operation

ChangeFileOperation for creating, updating or deleting a file

*This model accepts additional fields of type Any.*

## Structure

`ChangeFileOperation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | new or updated file content, it must be base64 encoded |
| `from_path` | `str` | Optional | old path of the file to move |
| `operation` | [`Operation`](../../doc/models/operation.md) | Required | indicates what to do with the file: "create" for creating a new file, "update" for updating an existing file,<br>"upload" for creating or updating a file, "rename" for renaming a file, and "delete" for deleting an existing file. |
| `path` | `str` | Required | path to the existing or new file |
| `sha` | `str` | Optional | the blob ID (SHA) for the file that already exists, required for changing existing files |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.change_file_operation import ChangeFileOperation
from giteaapi.models.operation import Operation

change_file_operation = ChangeFileOperation(
    operation=Operation.UPDATE,
    path='path6',
    content='content6',
    from_path='from_path6',
    sha='sha8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

