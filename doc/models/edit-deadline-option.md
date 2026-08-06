
# Edit Deadline Option

EditDeadlineOption options for creating a deadline

*This model accepts additional fields of type Any.*

## Structure

`EditDeadlineOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `due_date` | `datetime` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.edit_deadline_option import EditDeadlineOption

edit_deadline_option = EditDeadlineOption(
    due_date=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

