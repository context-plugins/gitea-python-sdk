
# Type 2

Type indicates the type of the notification subject
Issue NotifySubjectIssue a issue is subject of an notification
Pull NotifySubjectPull a pull is subject of an notification
Commit NotifySubjectCommit a commit is subject of an notification
Repository NotifySubjectRepository a repository is subject of an notification

## Enumeration

`Type2`

## Fields

| Name |
|  --- |
| `ISSUE` |
| `PULL` |
| `COMMIT` |
| `REPOSITORY` |

## Example

```python
from giteaapi.models.type_2 import Type2

type_2 = Type2.COMMIT
```

