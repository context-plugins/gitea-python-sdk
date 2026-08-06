
# Issue Meta

IssueMeta basic issue information

*This model accepts additional fields of type Any.*

## Structure

`IssueMeta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `index` | `int` | Optional | - |
| `owner` | `str` | Optional | owner of the issue's repo |
| `repo` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.issue_meta import IssueMeta

issue_meta = IssueMeta(
    index=236,
    owner='owner2',
    repo='repo4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

