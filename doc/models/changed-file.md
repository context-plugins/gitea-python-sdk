
# Changed File

ChangedFile store information about files affected by the pull request

*This model accepts additional fields of type Any.*

## Structure

`ChangedFile`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additions` | `int` | Optional | The number of lines added to the file |
| `changes` | `int` | Optional | The total number of changes to the file |
| `contents_url` | `str` | Optional | The API URL to get the file contents |
| `deletions` | `int` | Optional | The number of lines deleted from the file |
| `filename` | `str` | Optional | The name of the changed file |
| `html_url` | `str` | Optional | The HTML URL to view the file changes |
| `previous_filename` | `str` | Optional | The previous filename if the file was renamed |
| `raw_url` | `str` | Optional | The raw URL to download the file |
| `status` | `str` | Optional | The status of the file change (added, modified, deleted, etc.) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.changed_file import ChangedFile

changed_file = ChangedFile(
    additions=124,
    changes=66,
    contents_url='contents_url8',
    deletions=208,
    filename='filename8',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

