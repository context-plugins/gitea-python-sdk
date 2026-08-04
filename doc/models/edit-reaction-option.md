
# Edit Reaction Option

EditReactionOption contain the reaction type

*This model accepts additional fields of type Any.*

## Structure

`EditReactionOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `content` | `str` | Optional | The reaction content (e.g., emoji or reaction type) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.edit_reaction_option import EditReactionOption

edit_reaction_option = EditReactionOption(
    content='content2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

