
# Git Entry

GitEntry represents a git tree

*This model accepts additional fields of type Any.*

## Structure

`GitEntry`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mode` | `str` | Optional | Mode is the file mode (permissions) |
| `path` | `str` | Optional | Path is the file or directory path |
| `sha` | `str` | Optional | SHA is the Git object SHA |
| `size` | `int` | Optional | Size is the file size in bytes |
| `mtype` | `str` | Optional | Type indicates if this is a file, directory, or symlink |
| `url` | `str` | Optional | URL is the API URL for this tree entry |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.git_entry import GitEntry

git_entry = GitEntry(
    mode='mode4',
    path='path2',
    sha='sha4',
    size=106,
    mtype='type2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

