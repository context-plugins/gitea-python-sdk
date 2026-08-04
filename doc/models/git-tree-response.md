
# Git Tree Response

GitTreeResponse returns a git tree

*This model accepts additional fields of type Any.*

## Structure

`GitTreeResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | `int` | Optional | Page is the current page number for pagination |
| `sha` | `str` | Optional | SHA is the tree object SHA |
| `total_count` | `int` | Optional | TotalCount is the total number of entries in the tree |
| `tree` | [`List[GitEntry]`](../../doc/models/git-entry.md) | Optional | Entries contains the tree entries (files and directories) |
| `truncated` | `bool` | Optional | Truncated indicates if the response was truncated due to size |
| `url` | `str` | Optional | URL is the API URL for this tree |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.git_entry import GitEntry
from giteaapi.models.git_tree_response import GitTreeResponse

git_tree_response = GitTreeResponse(
    page=56,
    sha='sha2',
    total_count=78,
    tree=[
        GitEntry(
            mode='mode6',
            path='path2',
            sha='sha4',
            size=110,
            mtype='type2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        GitEntry(
            mode='mode6',
            path='path2',
            sha='sha4',
            size=110,
            mtype='type2',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    truncated=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

