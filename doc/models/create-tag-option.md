
# Create Tag Option

CreateTagOption options when creating a tag

*This model accepts additional fields of type Any.*

## Structure

`CreateTagOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `str` | Optional | The message to associate with the tag |
| `tag_name` | `str` | Required | - |
| `target` | `str` | Optional | The target commit SHA or branch name for the tag |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_tag_option import CreateTagOption

create_tag_option = CreateTagOption(
    tag_name='tag_name4',
    message='message4',
    target='target2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

