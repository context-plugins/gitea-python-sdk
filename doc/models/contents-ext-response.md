
# Contents Ext Response

*This model accepts additional fields of type Any.*

## Structure

`ContentsExtResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dir_contents` | [`List[ContentsResponse]`](../../doc/models/contents-response.md) | Optional | DirContents contains directory listing when the path represents a directory |
| `file_contents` | [`ContentsResponse`](../../doc/models/contents-response.md) | Optional | ContentsResponse contains information about a repo's entry's (dir, file, symlink, submodule) metadata and content |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.contents_ext_response import ContentsExtResponse
from gitea.models.contents_response import ContentsResponse
from gitea.models.file_links_response import FileLinksResponse

contents_ext_response = ContentsExtResponse(
    dir_contents=[
        ContentsResponse(
            links=FileLinksResponse(
                git='git6',
                html='html6',
                mself='self4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            content='content6',
            download_url='download_url2',
            encoding='encoding4',
            git_url='git_url2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    file_contents=ContentsResponse(
        links=FileLinksResponse(
            git='git6',
            html='html6',
            mself='self4',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        content='content0',
        download_url='download_url6',
        encoding='encoding8',
        git_url='git_url6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

