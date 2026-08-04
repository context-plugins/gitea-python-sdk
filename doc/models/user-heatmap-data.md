
# User Heatmap Data

UserHeatmapData represents the data needed to create a heatmap

*This model accepts additional fields of type Any.*

## Structure

`UserHeatmapData`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `contributions` | `int` | Optional | - |
| `timestamp` | `int` | Optional | TimeStamp defines a timestamp |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.user_heatmap_data import UserHeatmapData

user_heatmap_data = UserHeatmapData(
    contributions=226,
    timestamp=10,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

