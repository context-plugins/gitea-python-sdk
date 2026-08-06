
# State 6

State indicates the current state of the notification subject
open NotifySubjectStateOpen is an open subject
closed NotifySubjectStateClosed is a closed subject
merged NotifySubjectStateMerged is a merged pull request

## Enumeration

`State6`

## Fields

| Name |
|  --- |
| `OPEN` |
| `CLOSED` |
| `MERGED` |

## Example

```python
from gitea.models.state_6 import State6

state_6 = State6.CLOSED
```

