
# Cron

Cron represents a Cron task

*This model accepts additional fields of type Any.*

## Structure

`Cron`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `exec_times` | `int` | Optional | The total number of times this cron task has been executed |
| `name` | `str` | Optional | The name of the cron task |
| `next` | `datetime` | Optional | The next scheduled execution time |
| `prev` | `datetime` | Optional | The previous execution time |
| `schedule` | `str` | Optional | The cron schedule expression (e.g., "0 0 * * *") |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.cron import Cron

cron = Cron(
    exec_times=192,
    name='name2',
    next=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    prev=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    schedule='schedule4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

