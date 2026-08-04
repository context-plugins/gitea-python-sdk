
# Delete Email Option

DeleteEmailOption options when deleting email addresses

*This model accepts additional fields of type Any.*

## Structure

`DeleteEmailOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `emails` | `List[str]` | Optional | email addresses to delete |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from giteaapi.models.delete_email_option import DeleteEmailOption

delete_email_option = DeleteEmailOption(
    emails=[
        'emails5'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

