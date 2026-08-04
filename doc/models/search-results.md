
# Search Results

SearchResults results of a successful search

*This model accepts additional fields of type Any.*

## Structure

`SearchResults`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`List[Repository]`](../../doc/models/repository.md) | Optional | Data contains the repository search results |
| `ok` | `bool` | Optional | OK indicates if the search was successful |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.repository import Repository
from giteaapi.models.search_results import SearchResults

search_results = SearchResults(
    data=[
        Repository(
            allow_fast_forward_only_merge=False,
            allow_manual_merge=False,
            allow_merge_commits=False,
            allow_merge_update=False,
            allow_rebase=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Repository(
            allow_fast_forward_only_merge=False,
            allow_manual_merge=False,
            allow_merge_commits=False,
            allow_merge_update=False,
            allow_rebase=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Repository(
            allow_fast_forward_only_merge=False,
            allow_manual_merge=False,
            allow_merge_commits=False,
            allow_merge_update=False,
            allow_rebase=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    ok=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

