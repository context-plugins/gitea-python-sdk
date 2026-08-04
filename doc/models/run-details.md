
# Run Details

RunDetails returns workflow_dispatch runid and url

*This model accepts additional fields of type Any.*

## Structure

`RunDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `html_url` | `str` | Optional | - |
| `run_url` | `str` | Optional | - |
| `workflow_run_id` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.run_details import RunDetails

run_details = RunDetails(
    html_url='html_url8',
    run_url='run_url4',
    workflow_run_id=200,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

