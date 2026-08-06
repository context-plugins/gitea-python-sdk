
# Merge Upstream Request

*This model accepts additional fields of type Any.*

## Structure

`MergeUpstreamRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `str` | Optional | - |
| `ff_only` | `bool` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.merge_upstream_request import MergeUpstreamRequest

merge_upstream_request = MergeUpstreamRequest(
    branch='branch6',
    ff_only=False,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

