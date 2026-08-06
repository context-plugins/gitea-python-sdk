
# Add Time Option

AddTimeOption options for adding time to an issue

*This model accepts additional fields of type Any.*

## Structure

`AddTimeOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `datetime` | Optional | - |
| `time` | `int` | Required | time in seconds |
| `user_name` | `str` | Optional | username of the user who spent the time working on the issue (optional) |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.add_time_option import AddTimeOption

add_time_option = AddTimeOption(
    time=108,
    created=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    user_name='user_name2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

