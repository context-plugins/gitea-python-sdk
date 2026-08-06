
# Gitignore Template Info

GitignoreTemplateInfo name and text of a gitignore template

*This model accepts additional fields of type Any.*

## Structure

`GitignoreTemplateInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | Name is the name of the gitignore template |
| `source` | `str` | Optional | Source contains the content of the gitignore template |
| `additional_properties` | `Dict[str, Any]` | Optional | - |

## Example

```python
import jsonpickle

from gitea.models.gitignore_template_info import GitignoreTemplateInfo

gitignore_template_info = GitignoreTemplateInfo(
    name='name4',
    source='source0',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```

