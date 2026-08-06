
# Issue Config Contact Link

*This model accepts additional fields of type Any.*

## Structure

`IssueConfigContactLink`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `about` | `str` | Optional | - |
| `name` | `str` | Optional | - |
| `url` | `str` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.issue_config_contact_link import IssueConfigContactLink

issue_config_contact_link = IssueConfigContactLink(
    about='about6',
    name='name0',
    url='url4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

