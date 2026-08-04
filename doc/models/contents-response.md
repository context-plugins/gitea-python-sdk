
# Contents Response

ContentsResponse contains information about a repo's entry's (dir, file, symlink, submodule) metadata and content

*This model accepts additional fields of type Any.*

## Structure

`ContentsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `links` | [`FileLinksResponse`](../../doc/models/file-links-response.md) | Optional | FileLinksResponse contains the links for a repo's file |
| `content` | `str` | Optional | `content` is populated when `type` is `file`, otherwise null |
| `download_url` | `str` | Optional | DownloadURL is the direct download URL for this file |
| `encoding` | `str` | Optional | `encoding` is populated when `type` is `file`, otherwise null |
| `git_url` | `str` | Optional | GitURL is the Git API URL for this blob or tree |
| `html_url` | `str` | Optional | HTMLURL is the web URL for this file or directory |
| `last_author_date` | `datetime` | Optional | - |
| `last_commit_message` | `str` | Optional | LastCommitMessage is the message of the last commit that affected this file |
| `last_commit_sha` | `str` | Optional | LastCommitSHA is the SHA of the last commit that affected this file |
| `last_committer_date` | `datetime` | Optional | - |
| `lfs_oid` | `str` | Optional | LfsOid is the Git LFS object ID if this file is stored in LFS |
| `lfs_size` | `int` | Optional | LfsSize is the file size if this file is stored in LFS |
| `name` | `str` | Optional | Name is the file or directory name |
| `path` | `str` | Optional | Path is the full path to the file or directory |
| `sha` | `str` | Optional | SHA is the Git blob or tree SHA |
| `size` | `int` | Optional | Size is the file size in bytes |
| `submodule_git_url` | `str` | Optional | `submodule_git_url` is populated when `type` is `submodule`, otherwise null |
| `target` | `str` | Optional | `target` is populated when `type` is `symlink`, otherwise null |
| `mtype` | `str` | Optional | `type` will be `file`, `dir`, `symlink`, or `submodule` |
| `url` | `str` | Optional | URL is the API URL for this file or directory |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.contents_response import ContentsResponse
from giteaapi.models.file_links_response import FileLinksResponse

contents_response = ContentsResponse(
    links=FileLinksResponse(
        git='git6',
        html='html6',
        mself='self4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    content='content8',
    download_url='download_url6',
    encoding='encoding4',
    git_url='git_url4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

