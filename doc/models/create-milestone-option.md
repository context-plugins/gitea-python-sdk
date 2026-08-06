
# Create Milestone Option

CreateMilestoneOption options for creating a milestone

*This model accepts additional fields of type Any.*

## Structure

`CreateMilestoneOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description provides details about the milestone |
| `due_on` | `datetime` | Optional | - |
| `state` | [`State1`](../../doc/models/state-1.md) | Optional | - |
| `title` | `str` | Optional | Title is the title of the new milestone |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from gitea.models.create_milestone_option import CreateMilestoneOption
from gitea.models.state_1 import State1

create_milestone_option = CreateMilestoneOption(
    description='description2',
    due_on=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=State1.OPEN,
    title='title6',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

