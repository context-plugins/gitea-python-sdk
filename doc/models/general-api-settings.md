
# General Api Settings

GeneralAPISettings contains global api settings exposed by it

*This model accepts additional fields of type Any.*

## Structure

`GeneralApiSettings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `default_git_trees_per_page` | `int` | Optional | DefaultGitTreesPerPage is the default number of Git tree items per page |
| `default_max_blob_size` | `int` | Optional | DefaultMaxBlobSize is the default maximum blob size for API responses |
| `default_max_response_size` | `int` | Optional | DefaultMaxResponseSize is the default maximum response size |
| `default_paging_num` | `int` | Optional | DefaultPagingNum is the default number of items per page |
| `max_response_items` | `int` | Optional | MaxResponseItems is the maximum number of items returned in API responses |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.general_api_settings import GeneralApiSettings

general_api_settings = GeneralApiSettings(
    default_git_trees_per_page=134,
    default_max_blob_size=186,
    default_max_response_size=102,
    default_paging_num=52,
    max_response_items=20,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

