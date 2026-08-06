
# Trust Model

TrustModel of the repository

## Enumeration

`TrustModel`

## Fields

| Name |
|  --- |
| `DEFAULT` |
| `COLLABORATOR` |
| `COMMITTER` |
| `COLLABORATORCOMMITTER` |

## Example

```python
from gitea.models.trust_model import TrustModel

trust_model = TrustModel.COMMITTER
```

