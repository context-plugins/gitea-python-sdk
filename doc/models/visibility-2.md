
# Visibility 2

Team visibility within the organization. "private" teams are only
listable by members and org owners; "limited" teams are listable by
any organization member; "public" teams are listable by any signed-in
user.
public TeamVisibilityPublic
limited TeamVisibilityLimited
private TeamVisibilityPrivate

## Enumeration

`Visibility2`

## Fields

| Name |
|  --- |
| `PUBLIC` |
| `LIMITED` |
| `PRIVATE` |

## Example

```python
from giteaapi.models.visibility_2 import Visibility2

visibility_2 = Visibility2.PUBLIC
```

