
# Issue Config

*This model accepts additional fields of type Any.*

## Structure

`IssueConfig`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blank_issues_enabled` | `bool` | Optional | - |
| `contact_links` | [`List[IssueConfigContactLink]`](../../doc/models/issue-config-contact-link.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.issue_config import IssueConfig
from gitea.models.issue_config_contact_link import IssueConfigContactLink

issue_config = IssueConfig(
    blank_issues_enabled=False,
    contact_links=[
        IssueConfigContactLink(
            about='about2',
            name='name2',
            url='url6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

