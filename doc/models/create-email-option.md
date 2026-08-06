
# Create Email Option

CreateEmailOption options when creating email addresses

*This model accepts additional fields of type Any.*

## Structure

`CreateEmailOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `emails` | `List[str]` | Optional | email addresses to add |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.create_email_option import CreateEmailOption

create_email_option = CreateEmailOption(
    emails=[
        'emails3',
        'emails4'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

