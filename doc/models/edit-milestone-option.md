
# Edit Milestone Option

EditMilestoneOption options for editing a milestone

*This model accepts additional fields of type Any.*

## Structure

`EditMilestoneOption`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `str` | Optional | Description provides updated details about the milestone |
| `due_on` | `datetime` | Optional | Deadline is the updated due date for the milestone |
| `state` | [`State3`](../../doc/models/state-3.md) | Optional | State indicates the updated state of the milestone |
| `title` | `str` | Optional | Title is the updated title of the milestone |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import dateutil.parser
import jsonpickle

from giteaapi.models.edit_milestone_option import EditMilestoneOption
from giteaapi.models.state_3 import State3

edit_milestone_option = EditMilestoneOption(
    description='description0',
    due_on=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=State3.OPEN,
    title='title4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

