
# Annotated Tag Object

AnnotatedTagObject contains meta information of the tag object

*This model accepts additional fields of type Any.*

## Structure

`AnnotatedTagObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sha` | `str` | Optional | The SHA hash of the tagged object |
| `mtype` | `str` | Optional | The type of the tagged object (e.g., commit, tree) |
| `url` | `str` | Optional | The URL to access the tagged object |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.annotated_tag_object import AnnotatedTagObject

annotated_tag_object = AnnotatedTagObject(
    sha='sha2',
    mtype='type6',
    url='url0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

