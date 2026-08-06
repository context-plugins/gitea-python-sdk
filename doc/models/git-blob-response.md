
# Git Blob Response

GitBlobResponse represents a git blob

*This model accepts additional fields of type Any.*

## Structure

`GitBlobResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | The content of the git blob (may be base64 encoded) |
| `encoding` | `str` | Optional | The encoding used for the content (e.g., "base64") |
| `lfs_oid` | `str` | Optional | The LFS object ID if this blob is stored in LFS |
| `lfs_size` | `int` | Optional | The size of the LFS object if this blob is stored in LFS |
| `sha` | `str` | Optional | The SHA hash of the git blob |
| `size` | `int` | Optional | The size of the git blob in bytes |
| `url` | `str` | Optional | The URL to access this git blob |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.git_blob_response import GitBlobResponse

git_blob_response = GitBlobResponse(
    content='content8',
    encoding='encoding6',
    lfs_oid='lfs_oid2',
    lfs_size=198,
    sha='sha0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

