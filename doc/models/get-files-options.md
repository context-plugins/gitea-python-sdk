
# Get Files Options

GetFilesOptions options for retrieving metadate and content of multiple files

*This model accepts additional fields of type Any.*

## Structure

`GetFilesOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `files` | `List[str]` | Optional | Files is the list of file paths to retrieve |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.get_files_options import GetFilesOptions

get_files_options = GetFilesOptions(
    files=[
        'files3'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

