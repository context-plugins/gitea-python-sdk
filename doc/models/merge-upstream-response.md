
# Merge Upstream Response

*This model accepts additional fields of type Any.*

## Structure

`MergeUpstreamResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merge_type` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.merge_upstream_response import MergeUpstreamResponse

merge_upstream_response = MergeUpstreamResponse(
    merge_type='merge_type4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

